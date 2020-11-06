---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: a7bffb3b1387c084ef3b29ad6feb3962c724278f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512692"
---
# <span data-ttu-id="e3204-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e3204-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="e3204-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3204-102">SYNOPSIS</span></span>
<span data-ttu-id="e3204-103">Configura l'estensione DSC in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3204-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3204-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3204-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3204-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3204-105">DESCRIPTION</span></span>
<span data-ttu-id="e3204-106">Il cmdlet **set-AzureRmVMDscExtension** configura l'estensione DSC (Desired state Configuration) di Windows PowerShell in una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3204-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="e3204-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3204-107">EXAMPLES</span></span>

### <span data-ttu-id="e3204-108">Esempio 1: impostare un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="e3204-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e3204-109">Questo comando imposta l'estensione DSC nella macchina virtuale denominata VM07 per scaricare Sample.ps1.zip dall'account di archiviazione denominato STG e dal contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3204-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="e3204-110">Il comando richiama la configurazione denominata ConfigName.</span><span class="sxs-lookup"><span data-stu-id="e3204-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="e3204-111">Il file Sample.ps1.zip è stato precedentemente caricato tramite **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e3204-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="e3204-112">Esempio 2: impostare un'estensione DSC con i dati di configurazione</span><span class="sxs-lookup"><span data-stu-id="e3204-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e3204-113">Questo comando imposta l'estensione nella macchina virtuale denominata VM13 per scaricare Sample.ps1.zip dall'account di archiviazione denominato STG e dal contenitore denominato WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e3204-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e3204-114">Comando la configurazione denominata ConfigName e specifica i dati di configurazione e gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="e3204-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e3204-115">Il file Sample.ps1.zip è stato precedentemente caricato tramite **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e3204-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="e3204-116">Esempio 3: impostare un'estensione DSC con i dati di configurazione con l'aggiornamento automatico</span><span class="sxs-lookup"><span data-stu-id="e3204-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="e3204-117">Questo comando imposta l'estensione nella macchina virtuale denominata VM22 per scaricare Sample.ps1.zip dall'account di archiviazione denominato STG e dal contenitore denominato WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e3204-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e3204-118">Il comando richiama la configurazione denominata ConfigName e specifica i dati di configurazione e gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="e3204-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e3204-119">Questo comando consente inoltre l'aggiornamento automatico del gestore dell'estensione alla versione più recente.</span><span class="sxs-lookup"><span data-stu-id="e3204-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="e3204-120">La Sample.ps1.zip è stata precedentemente caricata usando **Publish-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e3204-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="e3204-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3204-121">PARAMETERS</span></span>

### <span data-ttu-id="e3204-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="e3204-122">-ArchiveBlobName</span></span>
<span data-ttu-id="e3204-123">Specifica il nome del file di configurazione caricato in precedenza dal cmdlet Publish-AzureRmVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3204-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="e3204-124">-ArchiveContainerName</span></span>
<span data-ttu-id="e3204-125">Nome della specie del contenitore di archiviazione di Azure in cui si trova l'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e3204-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3204-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="e3204-127">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione che contiene l'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e3204-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="e3204-128">Questo parametro è facoltativo se l'account di archiviazione e la macchina virtuale si trovano entrambi nello stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3204-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="e3204-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3204-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="e3204-130">Specifica il nome dell'account di archiviazione di Azure usato per scaricare ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="e3204-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e3204-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="e3204-132">Specifica il suffisso dell'endpoint di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e3204-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="e3204-133">-AutoUpdate</span></span>
<span data-ttu-id="e3204-134">Specifica la versione del gestore di estensione specificata dal parametro *Version* .</span><span class="sxs-lookup"><span data-stu-id="e3204-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="e3204-135">Per impostazione predefinita, il gestore di estensione non viene aggiornato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e3204-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="e3204-136">Usa il parametro *AutoUpdate* per abilitare l'aggiornamento automatico del gestore dell'estensione alla versione più recente e quando è disponibile.</span><span class="sxs-lookup"><span data-stu-id="e3204-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="e3204-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="e3204-137">-ConfigurationArgument</span></span>
<span data-ttu-id="e3204-138">Specifica una tabella hash che contiene gli argomenti della funzione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e3204-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="e3204-139">-ConfigurationData</span></span>
<span data-ttu-id="e3204-140">Specifica il percorso di un file con estensione psd1 che specifica i dati per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="e3204-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="e3204-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e3204-141">-ConfigurationName</span></span>
<span data-ttu-id="e3204-142">Specifica il nome della configurazione invocata dall'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="e3204-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="e3204-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="e3204-143">-DataCollection</span></span>
<span data-ttu-id="e3204-144">Specifica il tipo di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="e3204-144">Specifies the data collection type.</span></span>
<span data-ttu-id="e3204-145">I valori accettabili per questo parametro sono: Enable e Disable.</span><span class="sxs-lookup"><span data-stu-id="e3204-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-146">-Force</span><span class="sxs-lookup"><span data-stu-id="e3204-146">-Force</span></span>
<span data-ttu-id="e3204-147">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e3204-147">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3204-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e3204-148">-Location</span></span>
<span data-ttu-id="e3204-149">Specifica il percorso dell'estensione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3204-149">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="e3204-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3204-150">-Name</span></span>
<span data-ttu-id="e3204-151">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="e3204-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e3204-152">Il valore predefinito è Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="e3204-152">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="e3204-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3204-153">-ResourceGroupName</span></span>
<span data-ttu-id="e3204-154">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3204-154">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-155">-Versione</span><span class="sxs-lookup"><span data-stu-id="e3204-155">-Version</span></span>
<span data-ttu-id="e3204-156">Specifica la versione dell'estensione DSC a cui Set-AzureRmVMDscExtension applica le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e3204-156">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="e3204-157">-VMName</span></span>
<span data-ttu-id="e3204-158">Specifica il nome della macchina virtuale in cui è installato il gestore di estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="e3204-158">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-159">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="e3204-159">-WmfVersion</span></span>
<span data-ttu-id="e3204-160">Specifica la versione WMF.</span><span class="sxs-lookup"><span data-stu-id="e3204-160">Specifies the WMF version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3204-161">-Confirm</span></span>
<span data-ttu-id="e3204-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3204-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3204-163">-WhatIf</span></span>
<span data-ttu-id="e3204-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3204-164">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e3204-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3204-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3204-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3204-166">CommonParameters</span></span>
<span data-ttu-id="e3204-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3204-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3204-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3204-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3204-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3204-169">INPUTS</span></span>

### <span data-ttu-id="e3204-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3204-170">None</span></span>
<span data-ttu-id="e3204-171">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e3204-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3204-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3204-172">OUTPUTS</span></span>

## <span data-ttu-id="e3204-173">Note</span><span class="sxs-lookup"><span data-stu-id="e3204-173">NOTES</span></span>

## <span data-ttu-id="e3204-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3204-174">RELATED LINKS</span></span>

[<span data-ttu-id="e3204-175">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e3204-175">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="e3204-176">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e3204-176">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="e3204-177">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3204-177">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)


