---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: f32b49e28f34b676c4154793ac37989b58b0c917
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866548"
---
# <span data-ttu-id="7686a-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7686a-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="7686a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7686a-102">SYNOPSIS</span></span>
<span data-ttu-id="7686a-103">Configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7686a-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7686a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7686a-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7686a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7686a-105">DESCRIPTION</span></span>
<span data-ttu-id="7686a-106">Il cmdlet **set-AzureRmVMDiagnosticsExtension** configura l'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7686a-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="7686a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7686a-107">EXAMPLES</span></span>

### <span data-ttu-id="7686a-108">Esempio 1: abilitare la diagnostica usando un account di archiviazione specificato in un file di configurazione di diagnostica</span><span class="sxs-lookup"><span data-stu-id="7686a-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="7686a-109">Questo comando usa un file di configurazione della diagnostica per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="7686a-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="7686a-110">Il file diagnostics_publicconfig.xml contiene la configurazione XML pubblica per l'estensione di diagnostica, incluso il nome dell'account di archiviazione a cui verranno inviati i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="7686a-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="7686a-111">L'account di archiviazione diagnostica deve essere nella stessa sottoscrizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7686a-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="7686a-112">Esempio 2: abilitare la diagnostica usando un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7686a-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="7686a-113">Questo comando usa il nome dell'account di archiviazione per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="7686a-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="7686a-114">Se la configurazione di diagnostica non specifica un nome dell'account di archiviazione o se si vuole ignorare il nome dell'account di archiviazione di diagnostica specificato nel file di configurazione, usare il parametro *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="7686a-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="7686a-115">L'account di archiviazione diagnostica deve essere nella stessa sottoscrizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7686a-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="7686a-116">Esempio 3: abilitare la diagnostica tramite il nome e la chiave dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7686a-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="7686a-117">Questo comando usa il nome dell'account di archiviazione e la chiave per abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="7686a-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="7686a-118">Se l'account di archiviazione diagnostica si trova in un abbonamento diverso rispetto alla macchina virtuale, abilitare l'invio dei dati di diagnostica all'account di archiviazione specificando esplicitamente il nome e la chiave.</span><span class="sxs-lookup"><span data-stu-id="7686a-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="7686a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7686a-119">PARAMETERS</span></span>

### <span data-ttu-id="7686a-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7686a-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7686a-121">Indica se questo cmdlet consente all'agente guest Azure di aggiornare automaticamente l'estensione a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="7686a-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="7686a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7686a-122">-DefaultProfile</span></span>
<span data-ttu-id="7686a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7686a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7686a-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="7686a-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="7686a-125">Specifica il percorso del file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="7686a-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="7686a-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7686a-126">-Location</span></span>
<span data-ttu-id="7686a-127">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7686a-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7686a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7686a-128">-Name</span></span>
<span data-ttu-id="7686a-129">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="7686a-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="7686a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7686a-130">-ResourceGroupName</span></span>
<span data-ttu-id="7686a-131">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7686a-131">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7686a-132">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="7686a-132">-StorageAccountEndpoint</span></span>
<span data-ttu-id="7686a-133">Specifica l'endpoint dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7686a-133">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="7686a-134">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7686a-134">-StorageAccountKey</span></span>
<span data-ttu-id="7686a-135">Specifica la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7686a-135">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="7686a-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7686a-136">-StorageAccountName</span></span>
<span data-ttu-id="7686a-137">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7686a-137">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="7686a-138">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="7686a-138">-StorageContext</span></span>
<span data-ttu-id="7686a-139">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7686a-139">Specifies the Azure storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7686a-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7686a-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="7686a-141">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7686a-141">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="7686a-142">Per ottenere la versione, eseguire il cmdlet Get-AzureRmVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="7686a-142">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="7686a-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="7686a-143">-VMName</span></span>
<span data-ttu-id="7686a-144">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7686a-144">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7686a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7686a-145">CommonParameters</span></span>
<span data-ttu-id="7686a-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7686a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7686a-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7686a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7686a-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7686a-148">INPUTS</span></span>

### <span data-ttu-id="7686a-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7686a-149">None</span></span>
<span data-ttu-id="7686a-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7686a-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7686a-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7686a-151">OUTPUTS</span></span>

### <span data-ttu-id="7686a-152">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7686a-152">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7686a-153">Note</span><span class="sxs-lookup"><span data-stu-id="7686a-153">NOTES</span></span>

## <span data-ttu-id="7686a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7686a-154">RELATED LINKS</span></span>

[<span data-ttu-id="7686a-155">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7686a-155">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="7686a-156">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="7686a-156">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="7686a-157">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7686a-157">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)


