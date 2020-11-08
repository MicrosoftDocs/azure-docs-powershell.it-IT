---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029911"
---
# <span data-ttu-id="1969e-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1969e-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="1969e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1969e-102">SYNOPSIS</span></span>
<span data-ttu-id="1969e-103">Elimina le credenziali di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="1969e-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="1969e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1969e-104">SYNTAX</span></span>

### <span data-ttu-id="1969e-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="1969e-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1969e-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="1969e-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1969e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1969e-107">DESCRIPTION</span></span>
<span data-ttu-id="1969e-108">Il cmdlet **Remove-AzureStorSimpleStorageAccountCredential** Elimina le credenziali di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="1969e-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="1969e-109">Specifica un account per nome o usa il cmdlet **Get-AzureStorSimpleStorageAccountCredential** per ottenere un oggetto **StorageAccountCredential** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1969e-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="1969e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1969e-110">EXAMPLES</span></span>

### <span data-ttu-id="1969e-111">Esempio 1: rimuovere una credenziale dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1969e-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="1969e-112">Questo comando rimuove le credenziali dell'account per l'account di archiviazione denominato ContosoStorage07.</span><span class="sxs-lookup"><span data-stu-id="1969e-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="1969e-113">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="1969e-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1969e-114">Il cmdlet rimuove le credenziali senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1969e-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="1969e-115">Esempio 2: rimuovere una credenziale dell'account di archiviazione usando l'operatore pipeline</span><span class="sxs-lookup"><span data-stu-id="1969e-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="1969e-116">Questo comando ottiene l'account di archiviazione denominato ContosoStorage07 usando il cmdlet **Get-AzureStorSimpleStorageAccountCredential** e quindi passa tale oggetto al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="1969e-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="1969e-117">Il cmdlet corrente rimuove le credenziali per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1969e-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="1969e-118">Questo comando specifica il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="1969e-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="1969e-119">Il cmdlet non restituisce il controllo alla console finché non completa l'operazione Remove.</span><span class="sxs-lookup"><span data-stu-id="1969e-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="1969e-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1969e-120">PARAMETERS</span></span>

### <span data-ttu-id="1969e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1969e-121">-Force</span></span>
<span data-ttu-id="1969e-122">Indica che questo cmdlet non richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="1969e-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1969e-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="1969e-123">-Profile</span></span>
<span data-ttu-id="1969e-124">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="1969e-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1969e-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="1969e-125">-SAC</span></span>
<span data-ttu-id="1969e-126">Specifica le credenziali, come oggetto **StorageAccountCredential** , da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1969e-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="1969e-127">Per ottenere un oggetto **StorageAccountCredential** , usa il cmdlet **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="1969e-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1969e-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1969e-128">-StorageAccountName</span></span>
<span data-ttu-id="1969e-129">Specifica il nome della credenziale dell'account di archiviazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1969e-129">Specifies the name of the storage account credential to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1969e-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="1969e-130">-WaitForComplete</span></span>
<span data-ttu-id="1969e-131">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1969e-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1969e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1969e-132">CommonParameters</span></span>
<span data-ttu-id="1969e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1969e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1969e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1969e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1969e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1969e-135">INPUTS</span></span>

### <span data-ttu-id="1969e-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1969e-136">StorageAccountCredential</span></span>
<span data-ttu-id="1969e-137">Questo cmdlet accetta un oggetto **StorageAccountCredential** usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1969e-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="1969e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1969e-138">OUTPUTS</span></span>

### <span data-ttu-id="1969e-139">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="1969e-139">TaskStatusInfo</span></span>
<span data-ttu-id="1969e-140">Questo cmdlet restituisce un oggetto **TaskStatusInfo** , se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="1969e-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="1969e-141">Note</span><span class="sxs-lookup"><span data-stu-id="1969e-141">NOTES</span></span>

## <span data-ttu-id="1969e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1969e-142">RELATED LINKS</span></span>

[<span data-ttu-id="1969e-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1969e-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="1969e-144">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1969e-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="1969e-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1969e-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="1969e-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="1969e-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


