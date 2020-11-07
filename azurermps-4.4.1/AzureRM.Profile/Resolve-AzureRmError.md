---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
ms.openlocfilehash: 13bcf2e0b7e194801c45f725f7376b804c4ca045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688261"
---
# <span data-ttu-id="47127-101">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="47127-101">Resolve-AzureRmError</span></span>

## <span data-ttu-id="47127-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47127-102">SYNOPSIS</span></span>
<span data-ttu-id="47127-103">Visualizzare informazioni dettagliate sugli errori di PowerShell, con dettagli estesi per gli errori di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="47127-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47127-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47127-104">SYNTAX</span></span>

### <span data-ttu-id="47127-105">AnyErrorParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47127-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzureRmError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47127-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="47127-106">LastErrorParameterSet</span></span>
```
Resolve-AzureRmError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47127-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47127-107">DESCRIPTION</span></span>
<span data-ttu-id="47127-108">Risolve e visualizza informazioni dettagliate sugli errori nella sessione di PowerShell corrente, incluso il punto in cui si è verificato l'errore nello script, la traccia dello stack e tutte le eccezioni interne e di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="47127-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="47127-109">Per gli errori di PowerShell in Azure è disponibile un dettaglio aggiuntivo nei problemi di servizio di debug, inclusi dettagli completi sulla richiesta e risposta del server che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="47127-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="47127-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47127-110">EXAMPLES</span></span>

### <span data-ttu-id="47127-111">Esempio 1: risolvere l'ultimo errore</span><span class="sxs-lookup"><span data-stu-id="47127-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzureRmError -Last

   HistoryId: 3


Message        : Run Login-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="47127-112">Ottenere informazioni dettagliate sull'ultimo errore.</span><span class="sxs-lookup"><span data-stu-id="47127-112">Get details of the last error.</span></span>

### <span data-ttu-id="47127-113">Esempio 2: risolvere tutti gli errori della sessione</span><span class="sxs-lookup"><span data-stu-id="47127-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzureRmError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Login-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="47127-114">Ottenere informazioni dettagliate su tutti gli errori che si sono verificati nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="47127-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="47127-115">Esempio 3: risolvere un errore specifico</span><span class="sxs-lookup"><span data-stu-id="47127-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzureRmError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="47127-116">Ottenere informazioni dettagliate sull'errore specificato.</span><span class="sxs-lookup"><span data-stu-id="47127-116">Get details of the specified error.</span></span>

## <span data-ttu-id="47127-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47127-117">PARAMETERS</span></span>

### <span data-ttu-id="47127-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47127-118">-DefaultProfile</span></span>
<span data-ttu-id="47127-119">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="47127-119">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47127-120">-Error</span><span class="sxs-lookup"><span data-stu-id="47127-120">-Error</span></span>
<span data-ttu-id="47127-121">Uno o più record di errore da risolvere.</span><span class="sxs-lookup"><span data-stu-id="47127-121">One or more error records to resolve.</span></span>  <span data-ttu-id="47127-122">Se non sono specificati parametri, vengono risolti tutti gli errori della sessione.</span><span class="sxs-lookup"><span data-stu-id="47127-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: System.Management.Automation.ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47127-123">-Last</span><span class="sxs-lookup"><span data-stu-id="47127-123">-Last</span></span>
<span data-ttu-id="47127-124">Risolvere solo l'ultimo errore che si è verificato nella sessione.</span><span class="sxs-lookup"><span data-stu-id="47127-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47127-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47127-125">CommonParameters</span></span>
<span data-ttu-id="47127-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47127-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47127-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47127-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47127-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47127-128">INPUTS</span></span>

### <span data-ttu-id="47127-129">System. Management. Automation. ErrorRecord []</span><span class="sxs-lookup"><span data-stu-id="47127-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="47127-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47127-130">OUTPUTS</span></span>

### <span data-ttu-id="47127-131">Microsoft. Azure. Commands. profile. Errors. AzureErrorRecord</span><span class="sxs-lookup"><span data-stu-id="47127-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>
<span data-ttu-id="47127-132">Informazioni su un errore di PowerShell che non implica un excpetion.</span><span class="sxs-lookup"><span data-stu-id="47127-132">Information about a powershell error that does not involve an excpetion.</span></span>

### <span data-ttu-id="47127-133">Microsoft. Azure. Commands. profile. Errors. AzureExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="47127-133">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>
<span data-ttu-id="47127-134">Informazioni su un errore che include informazioni dettagliate sull'eccezione che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="47127-134">Information about an error including detailed information on the exception that raised the error.</span></span>

### <span data-ttu-id="47127-135">Microsoft. Azure. Commands. profile. Errors. AzureRestExceptionRecord</span><span class="sxs-lookup"><span data-stu-id="47127-135">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>
<span data-ttu-id="47127-136">Informazioni sugli errori nelle comunicazioni di cleint/server.</span><span class="sxs-lookup"><span data-stu-id="47127-136">Information about errors in cleint/server communications.</span></span>  <span data-ttu-id="47127-137">Questa operazione contiene spesso informazioni importanti sull'errore dal server.</span><span class="sxs-lookup"><span data-stu-id="47127-137">This will often contain important information about the error from the server.</span></span>

## <span data-ttu-id="47127-138">Note</span><span class="sxs-lookup"><span data-stu-id="47127-138">NOTES</span></span>

## <span data-ttu-id="47127-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47127-139">RELATED LINKS</span></span>

