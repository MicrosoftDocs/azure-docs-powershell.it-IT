---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023640"
---
# <span data-ttu-id="1a0fe-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1a0fe-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="1a0fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0fe-103">Consente la diagnostica delle applicazioni in un sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="1a0fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a0fe-104">SYNTAX</span></span>

### <span data-ttu-id="1a0fe-105">Fileparameterst</span><span class="sxs-lookup"><span data-stu-id="1a0fe-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a0fe-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a0fe-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a0fe-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a0fe-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a0fe-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a0fe-108">DESCRIPTION</span></span>
<span data-ttu-id="1a0fe-109">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1a0fe-110">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1a0fe-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1a0fe-111">Consente la diagnostica delle applicazioni in un sito Web di Azure e consente di configurare l'archiviazione dei log in un file System o in uno spazio di archiviazione Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="1a0fe-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a0fe-112">EXAMPLES</span></span>

### <span data-ttu-id="1a0fe-113">Esempio 1: abilitare la diagnostica tramite file System</span><span class="sxs-lookup"><span data-stu-id="1a0fe-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="1a0fe-114">Questo esempio consente la registrazione delle applicazioni nel file System con livello dettagliato.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="1a0fe-115">Esempio 2: abilitare la registrazione con l'archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="1a0fe-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="1a0fe-116">Questo esempio Abilita la registrazione delle applicazioni con l'account di archiviazione denominato account con il livello di registrazione impostato su informazioni.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="1a0fe-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a0fe-117">PARAMETERS</span></span>

### <span data-ttu-id="1a0fe-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="1a0fe-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-119">-File</span><span class="sxs-lookup"><span data-stu-id="1a0fe-119">-File</span></span>
<span data-ttu-id="1a0fe-120">Specifica che si vuole usare un file System per archiviare i file di log.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="1a0fe-121">-LogLevel</span></span>
<span data-ttu-id="1a0fe-122">Livello di log da archiviare.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-122">The log level to store.</span></span>
<span data-ttu-id="1a0fe-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1a0fe-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a0fe-124">Errore</span><span class="sxs-lookup"><span data-stu-id="1a0fe-124">Error</span></span>
- <span data-ttu-id="1a0fe-125">Avviso</span><span class="sxs-lookup"><span data-stu-id="1a0fe-125">Warning</span></span>
- <span data-ttu-id="1a0fe-126">Informazioni</span><span class="sxs-lookup"><span data-stu-id="1a0fe-126">Information</span></span>
- <span data-ttu-id="1a0fe-127">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="1a0fe-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a0fe-128">-Name</span></span>
<span data-ttu-id="1a0fe-129">Specifica il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-129">Specifies the name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a0fe-130">-PassThru</span></span>
<span data-ttu-id="1a0fe-131">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1a0fe-132">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1a0fe-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="1a0fe-133">-Profile</span></span>
<span data-ttu-id="1a0fe-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a0fe-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a0fe-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="1a0fe-136">-Slot</span></span>
<span data-ttu-id="1a0fe-137">Specifica il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-137">Specifies the name of the slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1a0fe-138">-StorageAccountName</span></span>
<span data-ttu-id="1a0fe-139">Account di archiviazione da usare per l'archiviazione dei log.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="1a0fe-140">Se non viene specificato, viene usato il CurrentStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="1a0fe-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="1a0fe-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="1a0fe-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0fe-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0fe-144">CommonParameters</span></span>
<span data-ttu-id="1a0fe-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0fe-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0fe-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a0fe-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0fe-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a0fe-147">INPUTS</span></span>

## <span data-ttu-id="1a0fe-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a0fe-148">OUTPUTS</span></span>

## <span data-ttu-id="1a0fe-149">Note</span><span class="sxs-lookup"><span data-stu-id="1a0fe-149">NOTES</span></span>

## <span data-ttu-id="1a0fe-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a0fe-150">RELATED LINKS</span></span>

[<span data-ttu-id="1a0fe-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1a0fe-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="1a0fe-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a0fe-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="1a0fe-153">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a0fe-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1a0fe-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a0fe-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1a0fe-155">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a0fe-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


