<p align='center'>
    <img width=700 src=https://summerofcode.withgoogle.com/assets/media/logo.svg>
    <br><br><br>
    <img width=200 src="https://res.cloudinary.com/crunchbase-production/image/upload/c_lpad,h_256,w_256,f_auto,q_auto:eco,dpr_1/v1401072286/v42evvabnvzdqupnlqdi.png">
    <br><br>
    <center><h1>GSOC'23 PROPOSAL - Mifos Initiative</h1></center>
    <center><h2><b>Mifos Mobile 6.0 - Mobile Banking App
</b></h2></center>
    <br><br><br>
</p>

Organization: [Mifos Initiative](https://mifos.org/)

Project Name: [Mifos Mobile 6.0 - Mobile Banking App](https://mifosforge.jira.com/wiki/spaces/RES/pages/3296690177/Google+Summer+of+Code+2023+Ideas#Mifos-Mobile-6.0---Mobile-Banking-App)

Candidate Name: Pratyush Singh

Expected Project Size: 350 hours

Mentors: 
- [Ahmad Jawid Muhammadi](https://github.com/jawidMuhammadi) 
- [Garvit Agarwal](https://github.com/garvit984)
- [Saksham Handu](https://github.com/miPlodder)

<br><br><br><br><br><br><br><br>

# Contents     
- [Contents](#contents)
- [1. Project Idea](#1-project-idea)
- [2. Implementation of the idea ](#2-implementation-of-the-idea)   
    - [2.1 Migration from MVP to MVVM](#21-migration-from-mvp-to-mvvm) 
        - [2.1.1 Migrating an activity](#211-migrating-an-activity) 
        - [2.1.2 Migrating a fragment](#212-migrating-a-fragment)
    - [2.2 Basic Integration of Navigation Graph](#22-basic-integration-of-navigation-graph)
    - [2.3 Improving Github workflows](#23-improving-github-workflows)
    - [2.4 My Ideas for the app](#24-my-ideas-for-the-app)
        - [2.4.1 Migrating from Butter Knife to View Binding](#241-migrating-from-butter-knife-to-view-binding)
        - [2.4.2 Adding option to change connection settings from login page](#242-adding-option-to-change-connection-setting-from-login-page)
- [3. Week Wise Breakdown](#3-week-wise-breakdown)
    - [3.1 Community Bonding Period (4 May - 28 May)](#31-community-bonding-period-4-may---28-may)
        - [Week 1](#week-1)
        - [Week 2](#week-2) 
        - [Week 3](#week-3)
    - [3.2 Phase 1 (29 May - 9 July)](#32-phase-1-29-may---9-july)<!--  TODO along with the breakdown image -->
        - [Week 4](#week-4)
        - [Week 5](#week-5)
        - [Week 6](#week-6)
        - [Week 7](#week-7)
        - [Week 8 and rest of phase 1](#week-8-and-rest-of-phase-1)
    - [3.3 Phase 2 (14 July - 21 Aug)](#33-phase-2-14-july---21-aug)<!--  TODO along with the breakdown image -->
        - [Week 10](#week-10)
        - [Week 11](#week-11)
        - [Week 12](#week-12)
        - [Week 13](#week-13)
        - [Week 14](#week-14)
        - [Week 15 and the rest of phase 2 ](#week-15-and-rest-of-phase-2)
    - [3.4 Post phase 2 (After Aug 28)](#34-post-phase-2-after-aug-28)
- [4. Why Am I The Right Person](#4-why-am-i-the-right-person)
- [5. Current Area of Study](#5-current-area-of-study)
- [6. Contact Information](#6-contact-information)
- [7. Career Goals](#7-career-goals)
- [8. Source Code I have written](#8-project-source-code-i-have-written)
- [9. Gitter Channel](#9-gitter-channel)
- [10. Other Open Source Contributions](#10-other-open-source-contributions)
- [11. Experience with Angular/Java/Spring/Hibernate/MySQL/Android](#11-experience-with-angularjavaspringhibernatemysqlandroid)
- [12. Other Commitments](#12-other-commitments)
- [13. Contributions To Mifos](#13-contributions-to-mifos)
- [14. What motivates me to work with mifos](#14-what-motivates-to-work-with-mifos-for-gsoc)
- [15. Previous Participation in GSoc](#15-previous-participation-in-gsoc)
- [16. Application to multiple Orgs](#16-application-to-multiple-orgs)
<br><br><br><br><br><br><br><br><br><br><br><br>


# 1. Project Idea
I wish to contribute to Mifos Mobile 6.0 - Mobile Banking App

Abstract
- 

- Replace API layer from self-service Fineract APIs to Open Banking APIs
- Complete Support for customer support/chat via RocketChat
- Integration with an external payment system (Mojaloop, mPesa) via our payment hub. 
- Migrate Dagger to Hilt
- Migrate from MVP to MVVM-Clean architecture (Not the whole project, maybe 20-30%)
- The basic integration of the Navigation Graph in the project
- The basic integration of Coroutines
- Continue adding unit tests for Data Layer and UI Layer
- Cover all the screens with UI tests
- Improve Githhub workflows and add jobs to run Unit and UI tests
<!-- - Basic integration of Jetpack Compose -->

<br>

# 2. Implementation of the idea
<!-- ## 2.1 Support for customer support/chat via RocketChat
- Customer support enhances users experience with realtime conversations.App users sometimes experience issues when using the app itself. In-app chat will enable us to support them right away and provide a native user and customer experience.This will help us with product stickiness and also increase customers service productivity .

<br>

## 2.2 Migration from Dagger to Hilt
- Hilt makes working with AndroidX a lot easier by removing that boilerplate code. What’s even better is that you don’t even need to inject the Factory in the Android framework class, you call it as if Hilt wasn’t there. With @ViewModelInject, Hilt generates the right ViewModelProvider.Factory for you that @AndroidEntryPoint activities and fragments can use directly.

<br> -->

## 2.1 Migration from MVP to MVVM
The MVVM architecture is designed to store and manage UI-related data in a lifecycle conscious way. Configuration changes such as screen rotations are handled properly by ViewModels.It separates the responsibilities of the user interface from the business logic, which makes the code easier to maintain and test.Because the ViewModel is decoupled from the View, it can be unit tested without the need for a graphical user interface (GUI). This makes testing faster and more reliable.MVVM leverages data binding to establish a connection between the View and ViewModel. This means that changes made to the ViewModel are automatically reflected in the View, and vice versa. This reduces the amount of boilerplate code needed to keep the UI up-to-date.Because the ViewModel contains the business logic, changes to the UI can be made without affecting the underlying data or business logic. This makes it easier to maintain and extend the code over time.
### 2.1.1 Migrating an Activity 
- In the original code, all the business logic was in the SplashActivity class. This violates the separation of concerns principle, which states that each class should have a single responsibility. In the MVVM architecture, the ViewModel is responsible for holding the data and the business logic, while the View (in this case, the SplashActivity) is responsible for displaying the data and handling user interactions.

- So, to follow this principle, we create a separate SplashViewModel class that holds the business logic, and move the logic from the SplashActivity to the SplashViewModel. This way, the SplashActivity is only responsible for displaying the data returned by the SplashViewModel, and the SplashViewModel is responsible for deciding what data to return and how to generate it.

- The SplashViewModelFactory is used to create an instance of the SplashViewModel. We use a Factory instead of directly creating a new instance of the ViewModel class because the ViewModel class has a lifecycle that is tied to the lifecycle of the View (i.e., the SplashActivity), and the Factory ensures that we always get the same instance of the ViewModel even if the View is recreated due to configuration changes like screen rotation. The Factory creates the ViewModel using the PasscodePreferencesHelper object as a constructor parameter, so that the ViewModel has access to the data it needs to generate the appropriate Intent.
Below is the code for SplashViewModel.kt
<!-- - ![SplashViewModel.kt](./Screenshot%202023-03-07%20002127.png) -->
```xml
import android.content.Intent
import androidx.lifecycle.MutableLiveData
import androidx.lifecycle.ViewModel
import com.mifos.mobile.passcode.utils.PasscodePreferencesHelper
import kotlinx.coroutines.CoroutineScope
import kotlinx.coroutines.Dispatchers
import kotlinx.coroutines.launch

class SplashViewModel(private val passcodePreferencesHelper: PasscodePreferencesHelper) : ViewModel() {
    var intent: Intent?=null
    val liveData : MutableLiveData<String> = MutableLiveData()
    fun getDestinationIntent() {
        CoroutineScope(Dispatchers.IO).launch{
            if (passcodePreferencesHelper.passCode.isNotEmpty()) {
                liveData.postValue("Yes")
            } else {
                liveData.postValue("No")
            }
        }
    }
}
```  
Below is the code for SplashViewModelFactory.kt:
``` xml
import androidx.lifecycle.ViewModel
import androidx.lifecycle.ViewModelProvider
import com.mifos.mobile.passcode.utils.PasscodePreferencesHelper

class SplashViewModelFactory(private val passcodePreferencesHelper: PasscodePreferencesHelper) : ViewModelProvider.Factory {
    override fun <T : ViewModel> create(modelClass: Class<T>): T {
        return SplashViewModel(passcodePreferencesHelper) as T
    }
}
```
<br><br><br><br>

Refactored code for SplashActivity.kt :
```xml
class SplashActivity : BaseActivity() {

    private lateinit var viewModel: SplashViewModel

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        activityComponent?.inject(this)
        val passcodePreferencesHelper = PasscodePreferencesHelper(this)
        viewModel = ViewModelProvider(this, SplashViewModelFactory(passcodePreferencesHelper)).get(
            SplashViewModel::class.java)

        viewModel.getDestinationIntent()
        viewModel.liveData.observe(this){
            if (it.equals("Yes")){
                val i=(Intent(this,PassCodeActivity::class.java))
                i.putExtra(Constants.INTIAL_LOGIN,true)
                startActivity(i)
                finish()
            }
            else {
                startActivity(Intent(this,LoginActivity::class.java))
                finish()
            }
        }
    }
}
```
### 2.1.2 Migrating a fragment
- I have converted the LocationsFragment from MVP to MVVM because the MVVM pattern separates the business logic from the view, making the code more modular and easier to test.In the MVP pattern, the presenter is responsible for handling the business logic and updating the view, which can lead to tight coupling between the view and the presenter. This can make the code harder to maintain and test.

- In the MVVM pattern, the view model is responsible for handling the business logic, while the view is responsible for displaying the data. This separation of concerns makes the code more modular and easier to test.To convert the LocationsFragment from MVP to MVVM, I removed any reference to the presenter and created a view model to handle the business logic.

- In the LocationsViewModel class, I created two methods to handle the logic previously handled by the presenter. These methods receive the GoogleMap instance as a parameter and use it to add a marker and animate the camera to the headquarter location. In the LocationsFragment, I removed the onCreateView() method from the MVP implementation and created a viewModel property that is initialized in the onCreateView() method. I also removed the addMarker() and addAnimationToHeadquarter() methods and called the corresponding methods in the viewModel instance from the onMapReady() method.

Overall, the MVVM implementation is more modular and easier to test, as the business logic is separated from the view.<br>
Below is the LocationsViewModel.kt :
``` xml
import androidx.lifecycle.ViewModel
import com.google.android.gms.maps.CameraUpdateFactory
import com.google.android.gms.maps.GoogleMap
import com.google.android.gms.maps.model.LatLng
import com.google.android.gms.maps.model.MarkerOptions
import org.mifos.mobile.MifosSelfServiceApp.Companion.context
import org.mifos.mobile.R

class LocationsViewModel : ViewModel() {

    private val headquarterLatLng = LatLng(47.61115, -122.34481)

    fun addMarker(googleMap: GoogleMap) {
        googleMap.addMarker(
            MarkerOptions().position(headquarterLatLng)
            .title(context?.getString(R.string.mifos_initiative)))
    }

    fun addAnimationToHeadquarter(googleMap: GoogleMap) {
        googleMap.animateCamera(CameraUpdateFactory.newLatLngZoom(headquarterLatLng, 16.0f))
    }
}
```
Below is the modified LocationsFragment.kt : 
```xml
import android.os.Bundle
import android.util.Log
import android.view.LayoutInflater
import android.view.View
import android.view.ViewGroup
import androidx.lifecycle.ViewModelProvider
import butterknife.BindView
import butterknife.ButterKnife
import com.google.android.gms.maps.*
import org.mifos.mobile.R
import org.mifos.mobile.ui.fragments.base.BaseFragment
import org.mifos.mobile.viewModels.LocationsViewModel

class LocationsFragment : BaseFragment(), OnMapReadyCallback {

    private lateinit var viewModel: LocationsViewModel

    @BindView(R.id.map)
    lateinit var mapView: MapView

    override fun onCreateView(inflater: LayoutInflater, container: ViewGroup?,
                              savedInstanceState: Bundle?): View? {
        val rootView = inflater.inflate(R.layout.fragment_locations, container, false)
        ButterKnife.bind(this, rootView)

        mapView.onCreate(savedInstanceState)
        mapView.onResume()

        try {
            MapsInitializer.initialize(requireContext())
        } catch (e: Exception) {
            Log.d(LocationsFragment::class.java.simpleName, e.toString())
        }

        mapView.getMapAsync(this)

        viewModel = ViewModelProvider(this).get(LocationsViewModel::class.java)

        return rootView
    }

    override fun onMapReady(googleMap: GoogleMap) {
        viewModel.addMarker(googleMap)
        viewModel.addAnimationToHeadquarter(googleMap)
    }
    companion object {
        fun newInstance(): LocationsFragment {
            return LocationsFragment()
        }
    }
}
```
## 2.2 Basic Integration of Navigation Graph 
- The Navigation Component in Android provides a framework for implementing navigation between screens in an application. It uses a Navigation Graph, which is an XML file that defines the navigation paths and destinations in an app.The first step in integrating the Navigation Graph is to create the graph file and define the navigation paths and destinations. This can be done using Android Studio's Navigation Editor, which provides a visual interface for designing the graph.
- Once the Navigation Graph is created, the next step is to integrate it into the app's code. This involves using the Navigation Component APIs to load and navigate to the appropriate destination based on user input.
- As an example , I have taken up SettingsFragment and UpdatePasswordFragment . To implement a navigation graph I have added these two files in the xml and defined an action from SettingsFragment to the UpdatePasswordFragment.Having done this, I added a **FragmentContainerView** in the SettingsActivity that will act as my NavHost. <br><br><br>
- The appropriate changes in `activity_settings.xml` is : 
```xml
 <androidx.fragment.app.FragmentContainerView
            android:id="@+id/fragmentContainerView"
            android:name="androidx.navigation.fragment.NavHostFragment"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            app:defaultNavHost="true"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintHorizontal_bias="0.0"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            app:layout_constraintVertical_bias="0.0"
            app:navGraph="@navigation/nav_frags" />

```
- Now we do not need `replaceFragment(SettingsFragment.newInstance(), false,R.id.fragmentContainerView)` in the SettingsActivity.We now just need to do one last change in the SettingsFragment i.e. we need to add findNavController.
- The change in the SettingsFragment is :
```xml
override fun onPreferenceTreeClick(preference: Preference): Boolean {
        when (preference.key) {
            Constants.PASSWORD -> findNavController().navigate(R.id.action_settingsFragment_to_updatePasswordFragment)
        }
        return super.onPreferenceTreeClick(preference)
    }
```
- I have taken this just to show it as demo and I can add a few more navigation graphs that would make the app further scalable. For instance , currently we have a **LoginActivity** and a **RegisterationActivity** .But the role of the **RegisterationActivity** is just to replace the fragment which is **RegisterationFragment**. We can get rid of the two activities and replace them by just one activity let's say **AuthenticationActivity** and convert the **LoginActivity** to a fragment.
- So now you will have just one Activity and on top of that you will have two fragments that can be added in another navigation graph.
<br>

<!-- ## 2.5 Basic integration of coroutines

<br>

## 2.7 Unit Test 
<br> -->

## 2.3 Improving Github Workflows 
- Currently the workflows do not have any jobs that runs the Unit tests or the UI tests. Hence modifications in the workflow to allow both tests to run will be a good feature to have.By running unit tests and UI tests as part of our Github workflow, we can get early feedback on code changes and catch issues before they are merged into the main branch. This can help prevent bugs from being introduced into the production code.
- It can provide a faster feedback loop for developers and can help them iterate and develop features more quickly.By automating testing as part of your Github workflow, you can reduce the need for manual testing. This can save time and resources and allow developers to focus on other tasks.
- Job for Unit test would be :
```xml
unitTest:
    name: Unit Tests
    runs-on: ubuntu-latest
    steps:
      - name: Checking out repository
        uses: actions/checkout@v2

      - name: Run Unit Tests
        run: ./gradlew testDebugUnitTest

      - name: Upload Test Report
        uses: actions/upload-artifact@v2.2.2
        if: always()
        with:
          name: Unit Test Report
          path: app/build/reports/tests/testDebugUnitTest/
```
Job for UI tests would be :
```xml
  uiTest:
    name: UI Tests
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Checking out repository
        uses: actions/checkout@v2

      - name: Start Emulator
        uses: reactivecircus/android-emulator-runner@v2
        with:
          api-level: 29
          arch: x86
          profile: Nexus 5X

      - name: Wait for Emulator to Start
        run: android-wait-for-emulator

      - name: Unlock Screen
        run: adb shell input keyevent 82

      - name: Run UI Tests
        run: ./gradlew connectedDebugAndroidTest

      - name: Upload Test Report
        uses: actions/upload-artifact@v2.2
```
- **unitTest job** : This job is responsible for running unit tests on the application's codebase. Unit tests are automated tests that check individual units or modules of an application in isolation to ensure that they are functioning correctly. The unitTest job runs the unit tests using the Gradle wrapper and a testing framework such as JUnit or Mockito.
- **uiTest job** :  This job is responsible for running UI tests on the application's user interface. UI tests are automated tests that simulate user interactions with the application to ensure that its UI is functioning correctly. The uiTest job runs the UI tests using a testing tool such as Espresso 

## 2.4 My Ideas for the app
There are certain features that are not currently present in the ideas list but in my opinion would look good and also be in accordance with the new android standards.
### 2.4.1 Migrating from Butter Knife to View Binding
- As the Android Development scene continues to grow, new build tools are created in order to address issues developers had seen using previous solutions. A commonly used tool was Butterknife. At the time, Butterknife was used to reduce the the amount of times the findViewById(...) function had been used in order to reference a view in your application. However, Butterknife still had its own issues such as null safety and speed. Now introduce View Binding: a low code, null safe, and fast binding tool! View Binding is a 1st party tool built by the Google Android Development team which helps reference and easily manage views within an app
- Butterknife is a 3rd party library made to address the issue of using findViewById(...) functions to reference and interact with views. It helped reduce boilerplate code but also had to set up a @Bind annotation every time you wanted to interact with a view. Then View Binding was introduced starting at Gradle version 3.6.This single binding variable allows us to access every view, set up event listeners, and any other functionality we'd do with Butterknife.
- On top of Butterknife being deprecated, another reason to switch is because View Binding is compile time safe and builds fast. As for findViewById(...), this way of referencing views will lead to so much unnecessary code that could be replaced with a View Binding variable.

- First step would be to upgrade the gradle version to 7.3.1 from 7.2.0 and then adding the dependency as: 
    > android {
    ...
    buildFeatures {
        viewBinding = true
    }
} <br>
Below is LoginActivity.kt after its migration from Butter Knife to View Binding:
```xml
package org.mifos.mobile.ui.activities

import android.content.Intent
import android.os.Bundle
import android.view.View
import android.widget.Toast
import org.mifos.mobile.R
import org.mifos.mobile.databinding.ActivityLoginBinding
import org.mifos.mobile.models.payload.LoginPayload
import org.mifos.mobile.presenters.LoginPresenter
import org.mifos.mobile.ui.activities.base.BaseActivity
import org.mifos.mobile.ui.views.LoginView
import org.mifos.mobile.utils.Constants
import org.mifos.mobile.utils.Network
import org.mifos.mobile.utils.Toaster

import javax.inject.Inject

/**
 * @author Vishwajeet
 * @since 05/06/16
 */
class LoginActivity : BaseActivity(), LoginView {

    @JvmField
    @Inject
    var loginPresenter: LoginPresenter? = null

    private lateinit var binding:ActivityLoginBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        activityComponent?.inject(this)
        setContentView(R.layout.activity_login)
        loginPresenter?.attachView(this)
        binding=ActivityLoginBinding.inflate(layoutInflater)
        val view = binding.root
        setContentView(view)
        binding.btnLogin.setOnClickListener {
            onLoginClicked()
        }
        binding.btnRegister.setOnClickListener {
            onRegisterClicked()
        }

    }

    /**
     * Called when Login is user has successfully logged in
     */
    override fun onLoginSuccess() {
        loginPresenter?.loadClient()
    }

    /**
     * Shows ProgressDialog when called
     */
    override fun showProgress() {
        showProgressDialog(getString(R.string.progress_message_login))
    }

    /**
     * Hides the progressDialog which is being shown
     */
    override fun hideProgress() {
        hideProgressDialog()
    }

    /**
     * Starts [PassCodeActivity]
     */
    override fun showPassCodeActivity(clientName: String?) {
        showToast(getString(R.string.toast_welcome, clientName))
        startPassCodeActivity()
    }

    /**
     * It is called whenever any error occurs while executing a request
     *
     * @param errorMessage Error message that tells the user about the problem.
     */
    override fun showMessage(errorMessage: String?) {
        showToast(errorMessage!!, Toast.LENGTH_LONG)
        binding.llLogin?.visibility = View.VISIBLE
    }

    override fun showUsernameError(error: String?) {
        binding.tilUsername?.error = error
    }

    override fun showPasswordError(error: String?) {
        binding.tilPassword?.error = error
    }

    override fun clearUsernameError() {
        binding.tilUsername?.isErrorEnabled = false
    }

    override fun clearPasswordError() {
        binding.tilPassword?.isErrorEnabled = false
    }

    /**
     * Called when Login Button is clicked, used for logging in the user
     */
    fun onLoginClicked() {
        val username = binding.tilUsername?.editText?.editableText.toString()
        val password = binding.tilPassword?.editText?.editableText.toString()
        if (Network.isConnected(this)) {
            val payload = LoginPayload()
            payload.username = username
            payload.password = password
            loginPresenter?.login(payload)
        } else {
            Toaster.show(binding.llLogin, getString(R.string.no_internet_connection))
        }
    }

    fun onRegisterClicked() {
        startActivity(Intent(this@LoginActivity, RegistrationActivity::class.java))
    }

    override fun onDestroy() {
        super.onDestroy()
        loginPresenter?.detachView()
    }

    /**
     * Starts [PassCodeActivity] with `Constans.INTIAL_LOGIN` as true
     */

    private fun startPassCodeActivity() {
        val intent = Intent(this@LoginActivity, PassCodeActivity::class.java)
        intent.putExtra(Constants.INTIAL_LOGIN, true)
        startActivity(intent)
        finish()
    }
}
```
Similar approach could be applied on the fragments as well .
### 2.4.2 Adding Option to Change Connection setting from login page
- Currently the when you go to **Settings** and then click on **Update Endpoint** and try to change the endpoint they user is sent back to the LoginActivity. And now the user cannot log in back because of the updated endpoint which might be incorrect.The user would then have to uninstall the app and then install it again just to gain access of the system.
- To overcome this there should be a support in the LoginActivity to change the **Connection Settings** that would allow the user to change the endpoint without having to uninstall the app. This would save the users time and would be a good feature to have.
- The implementation idea can be derived from **Android Client** that presently has this feature and the same can be replicated over in mifos mobile
<br>

# 3. Week Wise Breakdown
<br>

## 3.1 Community Bonding Period (4 May - 28 May)

### Week 1
- Get in touch with the developers and the mentor
- Introduction to the community, to the mentor and fix timings to communicate
- Discuss any suggestions and changes to the project. There could modifications, new additions or ammendments; it would be better to go over these early

### Week 2
- Go Thorugh Mifos-Mobile codebase 
- Take reference from android client and try to implement features that are currently absent in mifos-mobile
- Go through the Open Banking API and related documentations 

### Week 3
- Discuss the working of the existing application with the mentor. Discuss the implementations of the new features
- Go over the new design in detail and ask for changes and suggestions
- Discuss the changes that need to take place in the frontend to accomodate for the breaking changes


## 3.2 Phase 1 (29 May - 9 July)

### Week 4

- I will start off gradually with the migration from MVP to MVVM architectural style
- The order that I will follow is : 
    - Splash Activity
    - Login Activity
    - Registeration Fragment
    - PassCode Activity
    - HomeOld Fragment 
    - Home Fragment and so on
- This order is somewhat sequential and will be one of the first steps to be undertaken
- I would also take inputs from my mentors and if the need arises, change the order of the migration 

### Week 5

- I would dedicate this week for the implementation of the Navigation graph
- I would start off by grouping the fragments that are connected in a sequential flow of motion and map out a graph for the same in the xml
- This would require the addition of FragmentContainerView in certain activities which will allow further FragmentTransaction operations on the FragmentContainerView and providing a consistent timing for lifecycle events.

### Week 6

- This week would be reserved for the migration from dagger to hilt & also for the integration of coroutines in the project


### Week 7

- integration of payment hubs

### Week 8 and Rest of Phase 1

- *Buffer* for any pending tasks
- Prepare a report for evaluation
- Discuss brief plan for Phase 2 with the mentors


## 3.3 Phase 2 (14 July - 21 Aug)

### Week 10 

- Rocket chat will provide users with the support and facility of fast solutions to their queries. Rocket chat will provide users to communicate securely in real-time.
 <!-- refer rocket chat lib here https://gist.github.com/ShivangiSingh17/67b6041387c1e281caa7df23347f549e -->
- Shivangi singh had already updated the callbacks in the library and had further added lifecycle to decline requests . The library can be found [here](https://github.com/ShivangiSingh17/mifos-Rocket.Chat)
- Now all is left to be done is the integration into the project and I will integrate this once I get the updated *APIs* during the GSoC period


### Week 11 

- replace existing api layer 

### Week 12 

- Write unit tests for data layer and UI layer(mockito)

### Week 13 

- This week will be dedicated to performing the UI tests using espresso whose dependencies are already present in the gradle
- We will have decent amount of changes to the UI uptill here and hence tests that cover all the screens must be put in place
- This will ensure that the views are displayed correctly and look the way they're supposed to.Besides it will ensure that the interactions are handled correctly.

### Week 14 

- After writing all the unit tests I will add appropriate jobs in the existing workflow to run these tests
- Running tests regularly and automating the testing process can save a lot of time and prevent issues from arising in the codebase

### Week 15 and Rest of Phase 2

- If the mentors permit then I would like to implement my own ideas. Considering the ideas aren't that cumbersome it will work out even if its accomplished at the end of the project
- *Buffer* to complete any remaining tasks
- Prepare report for evaluation

## 3.4 Post Phase 2 (After Aug 28)
- Discuss the project's outcome with my mentors and devise a plan of action for future contributions
- Engage with members of the community to solicit feedback on project implementation and to identify possible add-on features


# 4. Why am I the right person ?
I have been doing Android Application Development for more than one year now. I have gained
proficiency in it by doing multiple Internships, several Open Source Contributions as well as
Hackathons.I am quite conversant with Android Architectural Components, MVVM, activities, fragments, support libraries, version control, Networking Services, Firebase, UI Development, Jetpack Compose etc.<br>
<!-- Below is a brief overview of my work experience : 
<ul> 
<b>1. Open Source Contributor,Dare2Change(SLoP 2022): </b>
<ul>
a. I was amongst one of the winners at SLoP, 2020 where I contributed for an app
called <a href="https://play.google.com/store/apps/details?id=com.dtc.inout2020_aimers">Dare2Change</a>
<br>
b.Implemented Material Intro View library in the app, which is similar to Spotlight
library.<br>
c. Worked on key features as well as with services and notifications.<br>
d. Revamped the complete UI of the application and introduced a dark mode theme.<br>
e. My contributions for Dare2Change : <a href="https://github.com/coder2699/Dare2Change/pulls?q=is%3Apr+author%3A%40me+">Check Here</a><br>
</ul>
</ul>  -->
<!-- <br> -->

# 5. Current area of study
I am pre final year student pursuing **Information Science and Engineering** at Dayananda Sagar College of Engineering.
<!-- Over the course my area of study have included :
- Learning the fundamentals of Java, Python and C++ along with Data Structures and Computer Architecture
- I have learnt to collect,store and analyze data using tools like SQL and Python
- My studies have focused on Information Retrieval systems such as Search Engines,Cross Language Information Retrieval and digital libraries
- Learning about the fundamentals of ML that included supervised and unsupervised learning,neureal networks and deep learning
- I have also had the privilege to learn about distributed systems, cloud computing, and virtualization technologies. -->

# 6. Contact Information 
**Name**: Pratyush Singh

**Email**: <aries.pratyush@gmail.com>

**LinkedIn**: [https://www.linkedin.com/in/Pratyush-Singh/](https://www.linkedin.com/in/pratyush-singh-9323ab20a/)

**GitHub**: [https://github.com/PratyushSingh07](https://github.com/PratyushSingh07)

**Gitter Id**: [Pratyush Singh](@pratyushsingh07-63388c746da03739849d52a7:gitter.im)

**Mobile Number**: +91 9693565684

**Time Zone**:  Indian Standard Time (GMT+5:30)
<br>

# 7. Career Goals
As an android developer my first and foremost goal is to master the Android SDK,Multithreading and other related technologies and create a portfolio of projects that would include personal projects, open source contributions, or projects done as part of my studies or work.
As I gain more experience , I would want to specialize in UI/UX design along with enterprise app development and seek out for leadership roles. 
I would sooner or later venture into AOSP and get a grasp of low level android as well and transition into a full stack mobile developer.
I am self taught like many other developers out there and Open Source Projects have played an integral part in my growth and thus I would give back to this android community by sharing my knowledge and expertise through blog posts, tutorials,speaking engagements and ofcourse by contributing to Open Source Projects.
<br>

# 8. Project (Source Code I have written)
<b>1. Cyclofit : </b><a href="https://github.com/PratyushSingh07/cyclofit"><i>Source Code</i></a><br>
- Cyclofit is a safety and health monitoring system for cyclists
- It tracks the heart rate,calories burnt, distance coverered and much more using the sensors integrated in a single
device.Our device has a proximity sensor that can track any incoming vehicle by monitoring it’s rate of change of speed.
The data such as the heart rate are displayed into the app through an api
- Worked with firestore , firebase , Coroutines created a community section in this app that implements a real time
database
-  Visualized data in form of graphs using <a href="https://github.com/PhilJay/MPAndroidChart">MPAndroidChart</a>
<br>

<b>2. NewsLive : </b><a href="https://github.com/PratyushSingh07/NewsApp"><i>Source Code</i></a><br>
- Developed an Android application using the NewsAPI.org API, Retrofit, MVVM architecture, Room database, and Coroutines. 
- Implemented background tasks and asynchronous operations using Coroutines, ensuring smooth app performance and user engagement.
- Integrated Room database to provide offline caching and storage of user preferences and data, reducing server requests and improving app speed and reliability
- Utilized MVVM architecture to separate concerns and increase code maintainability, as well as Retrofit to easily connect to the NewsAPI.org API and retrieve real-time news data.
<br>

# 9. Gitter Channel 
Yes, I have visited all of mifos's gitter channel and my id was <a href="(@pratyushsingh07-63388c746da03739849d52a7:gitter.im)">PratyushSingh07</a>
<br><br><br><br><br><br><br>

# 10. Other Open Source Contributions 
<!-- Add PR as link below and also mention the works if possible -->
<ul>
I have been contributing to Open Souce for quite some time and here are some of my contributions:
<br>
<b>1. Catroid </b><br>
<b>2. Paintroid </b><br>
<b>3. Anki-Droid </b><br>
<b>4. Dare2Change </b><br>
</ul>
<br>

# 11. Experience with Angular/Java/Spring/Hibernate/MySQL/Android 
Yes, I do have experience with Android and Java and have built projects centered around them. I have decent knowledge of MySQL and SQLite Databases.I haven't particularly worked with AngularJS but I am familiar with JavaScript and I have also used React.js framework to build a
<a href="https://github.com/PratyushSingh07/PathFindingVis/">Path finding visualizer</a>,So If needed I can learn AngularJS at a quick pace.
<br>

# 12. Other Commitments
1. College Exams
2. Course projects
   
These are going to be an integral part of my 6th semester activities. They are not going to affect my GSOC efforts.  
I will be able to deliver my commited number of hours per week without much hindrance.
<!-- I am fully committed to enhancing the Mifos mobile platform during the upcoming summer as I do not have any other conflicting commitments. -->
<!-- <br> -->

# 13. Contributions to Mifos 
Below are the links to my contributions : 
<ul>
1. <a href="https://github.com/openMF/mifos-mobile/pull/1901" >PR #1901: Finger Print Authentication in the Passcode Activity</a>
<br>
2. <a href="https://github.com/openMF/mifos-mobile/pull/1899" >PR #1899: Fixes App Crash if you click on the submit button without selecting product ID</a>
<br>
3. <a href="https://github.com/openMF/mifos-mobile/pull/1930" >PR #1930: Fixes 'Change Passcode' in Settings</a>
<br>
4. <a href="https://github.com/openMF/mifos-mobile/pull/1929" >PR #1929: Fixes background color of Passcode with the theme</a>
<br>
5. <a href="https://github.com/openMF/mifos-mobile/pull/1927" >PR #1927: Fixes the behaviour of filters throught the app</a>
<br>
6. <a href="https://github.com/openMF/mifos-mobile/pull/1926" >PR #1926: Modified Error message in case of wrong endpoint</a>
<br>
7. <a href="https://github.com/openMF/mifos-mobile/pull/1912" >PR #1912: Fixes Scrolling when in landscope mode</a>
<br>
8. <a href="https://github.com/openMF/mifos-mobile/pull/1910" >PR #1910: Fixes App Crash when orientation is changed to landscape mode</a>
<br>
9. <a href="https://github.com/openMF/mifos-mobile/pull/1908" >PR #1908: Fixes duplication in Material Auto Complete Text View</a>
<br>
10. <a href="https://github.com/openMF/mifos-mobile/pull/1905" >PR #1905: Allows User to enter the correct passcode even after three unsuccessful tries</a>
<br>
11. <a href="https://github.com/openMF/mifos-mobile/pull/1904" >PR #1904: Added Country Code Picker in the Signup form</a>
<br>
12. <a href="https://github.com/openMF/mifos-mobile/pull/1938" >PR #1938: Offline Support in the home fragment</a>
<br>
</ul>
<!-- <br>` -->

# 14. What motivates to work with Mifos for GSoC 
Mifos Initiative is making a significant difference in the world by providing financial inclusion to people who would otherwise be excluded from the formal financial system. This mission is truly inspiring, and being a part of it through the Google Summer of Code program is a privilege.
From a professional point of view mifos has a vibrant community of developers, volunteers, and supporters who are passionate about the mission of the organization. It's motivating to be a part of a community that is so dedicated to making a positive impact on the world.Besides
Google Summer of Code is a fantastic opportunity for students to gain real-world experience working on open-source projects. Mifos Initiative's participation in this program shows that they are committed to helping the next generation of developers like me succeed and contribute to something that would impact lives of billions around the globe.The work that we as a students do during the Google Summer of Code program can have a lasting impact on the Mifos Initiative and the people it serves. Knowing that the work you do can make a real difference in people's lives is incredibly rewarding.

Mifos Initiative's commitment to open-source software is essential for the sustainability of the financial inclusion ecosystem. By making their software freely available, they are enabling other organizations to provide financial services to underserved communities.
<br>

# 15. Previous Participation in GSoC
No,this is my first participation in Google Summer of Code
<br>

# 16. Application to multiple orgs
I will be applying only to Mifos-Mobile for this years' GSoC
<br>