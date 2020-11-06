---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: d93fd01fb178f093b6ed5527cca0c018cebe4f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518179"
---
# <span data-ttu-id="10431-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="10431-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="10431-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10431-102">SYNOPSIS</span></span>
<span data-ttu-id="10431-103">Configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10431-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10431-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10431-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [<CommonParameters>]
```

## <span data-ttu-id="10431-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10431-105">DESCRIPTION</span></span>
<span data-ttu-id="10431-106">Il cmdlet **set-AzureRmVMDiagnosticsExtension** configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10431-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="10431-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10431-107">EXAMPLES</span></span>

### <span data-ttu-id="10431-108">Esempio 1: abilitare la diagnostica usando un account di archiviazione specificato in un file di configurazione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="10431-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="10431-109">Questo comando usa un file di configurazione della diagnostica per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="10431-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="10431-110">Il file diagnostics_publicconfig.xml contiene la configurazione XML pubblica per l'estensione di diagnostica, incluso il nome dell'account di archiviazione a cui verranno inviati i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="10431-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="10431-111">L'account di archiviazione diagnostica deve essere nella stessa sottoscrizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10431-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="10431-112">Esempio 2: abilitare la diagnostica usando un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10431-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="10431-113">Questo comando usa il nome dell'account di archiviazione per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="10431-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="10431-114">Se la configurazione di diagnostica non specifica un nome dell'account di archiviazione o se si vuole ignorare il nome dell'account di archiviazione di diagnostica specificato nel file di configurazione, usare il parametro *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="10431-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="10431-115">L'account di archiviazione diagnostica deve essere nella stessa sottoscrizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10431-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="10431-116">Esempio 3: abilitare la diagnostica tramite il nome e la chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10431-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="10431-117">Questo comando usa il nome dell'account di archiviazione e la chiave per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="10431-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="10431-118">Se l'account di archiviazione diagnostica si trova in un abbonamento diverso rispetto alla macchina virtuale, abilitare l'invio dei dati di diagnostica all'account di archiviazione specificando esplicitamente il nome e la chiave.</span><span class="sxs-lookup"><span data-stu-id="10431-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="10431-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10431-119">PARAMETERS</span></span>

### <span data-ttu-id="10431-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="10431-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="10431-121">Indica se questo cmdlet consente all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="10431-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="10431-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="10431-123">Specifica il percorso del file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="10431-123">Specifies the path of the configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10431-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="10431-124">-Location</span></span>
<span data-ttu-id="10431-125">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10431-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="10431-126">-Name</span></span>
<span data-ttu-id="10431-127">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="10431-127">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10431-128">-ResourceGroupName</span></span>
<span data-ttu-id="10431-129">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10431-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-130">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="10431-130">-StorageAccountEndpoint</span></span>
<span data-ttu-id="10431-131">Specifica l'endpoint dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="10431-131">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="10431-132">-StorageAccountKey</span></span>
<span data-ttu-id="10431-133">Specifica la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="10431-133">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="10431-134">-StorageAccountName</span></span>
<span data-ttu-id="10431-135">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="10431-135">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-136">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="10431-136">-StorageContext</span></span>
<span data-ttu-id="10431-137">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="10431-137">Specifies the Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="10431-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="10431-139">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10431-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="10431-140">Per ottenere la versione, eseguire il cmdlet Get-AzureRmVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="10431-140">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="10431-141">-VMName</span></span>
<span data-ttu-id="10431-142">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10431-142">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10431-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10431-143">CommonParameters</span></span>
<span data-ttu-id="10431-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10431-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10431-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10431-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10431-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10431-146">INPUTS</span></span>

### <span data-ttu-id="10431-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="10431-147">None</span></span>
<span data-ttu-id="10431-148">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="10431-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10431-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10431-149">OUTPUTS</span></span>

## <span data-ttu-id="10431-150">Note</span><span class="sxs-lookup"><span data-stu-id="10431-150">NOTES</span></span>

## <span data-ttu-id="10431-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10431-151">RELATED LINKS</span></span>

[<span data-ttu-id="10431-152">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="10431-152">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="10431-153">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="10431-153">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="10431-154">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="10431-154">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)


