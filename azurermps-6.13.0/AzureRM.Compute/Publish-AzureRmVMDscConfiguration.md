---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
ms.openlocfilehash: 49dc91288c955de10c3dbcb84da74ffd3d71f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507580"
---
# <span data-ttu-id="6feac-101">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6feac-101">Publish-AzureRmVMDscConfiguration</span></span>

## <span data-ttu-id="6feac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6feac-102">SYNOPSIS</span></span>
<span data-ttu-id="6feac-103">Carica uno script DSC in archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="6feac-103">Uploads a DSC script to Azure blob storage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6feac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6feac-104">SYNTAX</span></span>

### <span data-ttu-id="6feac-105">UploadArchive (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6feac-105">UploadArchive (Default)</span></span>
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6feac-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="6feac-106">CreateArchive</span></span>
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6feac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6feac-107">DESCRIPTION</span></span>
<span data-ttu-id="6feac-108">Il cmdlet **Publish-AzureRmVMDscConfiguration** carica uno script DSC (Desired state Configuration) in Azure BLOB Storage, che in seguito può essere applicato alle macchine virtuali di Azure usando il cmdlet Set-AzureRmVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="6feac-108">The **Publish-AzureRmVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzureRmVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="6feac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6feac-109">EXAMPLES</span></span>

### <span data-ttu-id="6feac-110">Esempio 1: creare un pacchetto zip per caricarlo in Azure Storage</span><span class="sxs-lookup"><span data-stu-id="6feac-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="6feac-111">Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo carica in Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6feac-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="6feac-112">Esempio 2: creare un pacchetto zip e archiviarlo in un file locale</span><span class="sxs-lookup"><span data-stu-id="6feac-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="6feac-113">Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo archivia nel file locale denominato .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="6feac-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="6feac-114">Esempio 3: aggiungere la configurazione all'archivio e quindi caricarla nello spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6feac-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="6feac-115">Questo comando aggiunge la configurazione denominata Sample.ps1 all'archivio di configurazione per caricare in Azure Storage e ignora i moduli delle risorse dipendenti.</span><span class="sxs-lookup"><span data-stu-id="6feac-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="6feac-116">Esempio 4: aggiungere dati di configurazione e configurazione all'archivio e quindi caricarli in archiviazione</span><span class="sxs-lookup"><span data-stu-id="6feac-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="6feac-117">Questo comando aggiunge la configurazione denominata Sample.ps1 e i dati di configurazione denominati SampleData.psd1 nell'archivio di configurazione per caricare in Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6feac-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="6feac-118">Esempio 5: aggiungere configurazione, dati di configurazione e contenuto aggiuntivo all'archivio e quindi caricarlo nello spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6feac-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="6feac-119">Questo comando aggiunge la configurazione denominata Sample.ps1, i dati di configurazione SampleData.psd1 e il contenuto aggiuntivo all'archivio di configurazione per caricare in Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6feac-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="6feac-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6feac-120">PARAMETERS</span></span>

### <span data-ttu-id="6feac-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="6feac-121">-AdditionalPath</span></span>
<span data-ttu-id="6feac-122">Specifica il percorso di un file o di una directory da includere nell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="6feac-123">Viene scaricata nella macchina virtuale insieme alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="6feac-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="6feac-125">Specifica il percorso di un file con estensione psd1 che specifica i dati per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="6feac-126">Questa operazione viene aggiunta all'archivio di configurazione e quindi passata alla funzione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="6feac-127">Viene sovrascritto dal percorso dei dati di configurazione fornito tramite il cmdlet Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6feac-127">It gets overwritten by the configuration data path provided through the Set-AzureRmVMDscExtension cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="6feac-128">-ConfigurationPath</span></span>
<span data-ttu-id="6feac-129">Specifica il percorso di un file che contiene una o più configurazioni.</span><span class="sxs-lookup"><span data-stu-id="6feac-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="6feac-130">Il file può essere un file di script di Windows PowerShell (con estensione ps1) o un file di modulo di Windows PowerShell (con estensione psm1).</span><span class="sxs-lookup"><span data-stu-id="6feac-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="6feac-131">-ContainerName</span></span>
<span data-ttu-id="6feac-132">Specifica il nome del contenitore di archiviazione di Azure a cui è stata caricata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6feac-133">-DefaultProfile</span></span>
<span data-ttu-id="6feac-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6feac-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6feac-135">-Force</span><span class="sxs-lookup"><span data-stu-id="6feac-135">-Force</span></span>
<span data-ttu-id="6feac-136">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6feac-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="6feac-137">-OutputArchivePath</span></span>
<span data-ttu-id="6feac-138">Specifica il percorso di un file con estensione zip locale in cui scrivere l'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="6feac-139">Quando questo parametro viene usato, lo script di configurazione non viene caricato nell'archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="6feac-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6feac-140">-ResourceGroupName</span></span>
<span data-ttu-id="6feac-141">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="6feac-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="6feac-143">Indica che questo cmdlet esclude le dipendenze delle risorse DSC dall'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6feac-144">-StorageAccountName</span></span>
<span data-ttu-id="6feac-145">Specifica il nome dell'account di archiviazione di Azure usato per caricare lo script di configurazione nel contenitore specificato dal parametro *containerName* .</span><span class="sxs-lookup"><span data-stu-id="6feac-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="6feac-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="6feac-147">Specifica il suffisso per il punto finale dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6feac-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6feac-148">-Confirm</span></span>
<span data-ttu-id="6feac-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6feac-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6feac-150">-WhatIf</span></span>
<span data-ttu-id="6feac-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6feac-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6feac-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6feac-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feac-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6feac-153">CommonParameters</span></span>
<span data-ttu-id="6feac-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6feac-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6feac-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6feac-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6feac-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6feac-156">INPUTS</span></span>

### <span data-ttu-id="6feac-157">System. String</span><span class="sxs-lookup"><span data-stu-id="6feac-157">System.String</span></span>

### <span data-ttu-id="6feac-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="6feac-158">System.String[]</span></span>

## <span data-ttu-id="6feac-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6feac-159">OUTPUTS</span></span>

### <span data-ttu-id="6feac-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6feac-160">System.String</span></span>

## <span data-ttu-id="6feac-161">Note</span><span class="sxs-lookup"><span data-stu-id="6feac-161">NOTES</span></span>

## <span data-ttu-id="6feac-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6feac-162">RELATED LINKS</span></span>

[<span data-ttu-id="6feac-163">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6feac-163">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="6feac-164">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6feac-164">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="6feac-165">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6feac-165">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


