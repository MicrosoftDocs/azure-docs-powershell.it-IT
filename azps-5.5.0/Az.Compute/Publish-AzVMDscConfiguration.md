---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177631"
---
# <span data-ttu-id="292f4-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="292f4-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="292f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="292f4-102">SYNOPSIS</span></span>
<span data-ttu-id="292f4-103">Carica uno script DSC nell'archiviazione BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="292f4-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="292f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="292f4-104">SYNTAX</span></span>

### <span data-ttu-id="292f4-105">UploadArchive (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="292f4-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="292f4-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="292f4-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="292f4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="292f4-107">DESCRIPTION</span></span>
<span data-ttu-id="292f4-108">Il cmdlet **Publish-AzVMDscConfiguration** carica uno script DSC (Desired State Configuration) nell'archiviazione BLOB di Azure, che in seguito può essere applicato alle macchine virtuali di Azure usando il cmdlet Set-AzVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="292f4-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="292f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="292f4-109">EXAMPLES</span></span>

### <span data-ttu-id="292f4-110">Esempio 1: Creare un pacchetto ZIP e caricarlo nell'archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="292f4-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="292f4-111">Questo comando crea un pacchetto ZIP per lo script specificato e gli eventuali moduli delle risorse dipendenti e lo carica nell'archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="292f4-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="292f4-112">Esempio 2: Creare un pacchetto ZIP e archiviarlo in un file locale</span><span class="sxs-lookup"><span data-stu-id="292f4-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="292f4-113">Questo comando crea un pacchetto ZIP per lo script specificato e gli eventuali moduli delle risorse dipendenti e lo archivia nel file locale denominato .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="292f4-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="292f4-114">Esempio 3: Aggiungere la configurazione all'archivio e quindi caricarla nell'archiviazione</span><span class="sxs-lookup"><span data-stu-id="292f4-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="292f4-115">Questo comando aggiunge la configurazione denominata Sample.ps1 all'archivio di configurazione per caricarlo nell'archiviazione di Azure e ignora i moduli delle risorse dipendenti.</span><span class="sxs-lookup"><span data-stu-id="292f4-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="292f4-116">Esempio 4: Aggiungere i dati di configurazione e configurazione all'archivio e quindi caricarlo nell'archiviazione</span><span class="sxs-lookup"><span data-stu-id="292f4-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="292f4-117">Questo comando aggiunge la configurazione denominata Sample.ps1 e i dati di configurazione denominati SampleData.psd1 all'archivio di configurazione per caricarlo nell'archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="292f4-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="292f4-118">Esempio 5: Aggiungere la configurazione, i dati di configurazione e altri contenuti all'archivio e quindi caricarlo nell'archiviazione</span><span class="sxs-lookup"><span data-stu-id="292f4-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="292f4-119">Questo comando aggiunge la configurazione denominata Sample.ps1, i dati di configurazione SampleData.psd1 e altri contenuti all'archivio di configurazione per il caricamento in Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="292f4-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="292f4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="292f4-120">PARAMETERS</span></span>

### <span data-ttu-id="292f4-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="292f4-121">-AdditionalPath</span></span>
<span data-ttu-id="292f4-122">Specifica il percorso di un file o di una directory da includere nell'archivio della configurazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="292f4-123">Viene scaricata nella macchina virtuale insieme alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

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

### <span data-ttu-id="292f4-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="292f4-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="292f4-125">Specifica il percorso di un file psd1 che specifica i dati per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="292f4-126">Questa operazione viene aggiunta all'archivio di configurazione e quindi passata alla funzione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="292f4-127">Viene sovrascritta dal percorso dei dati di configurazione fornito tramite il cmdlet Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="292f4-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="292f4-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="292f4-128">-ConfigurationPath</span></span>
<span data-ttu-id="292f4-129">Specifica il percorso di un file contenente una o più configurazioni.</span><span class="sxs-lookup"><span data-stu-id="292f4-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="292f4-130">Il file può essere un file Windows PowerShell script (ps1) o un file Windows PowerShell module (psm1).</span><span class="sxs-lookup"><span data-stu-id="292f4-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

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

### <span data-ttu-id="292f4-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="292f4-131">-ContainerName</span></span>
<span data-ttu-id="292f4-132">Specifica il nome del contenitore di archiviazione di Azure in cui viene caricata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="292f4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292f4-133">-DefaultProfile</span></span>
<span data-ttu-id="292f4-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="292f4-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="292f4-135">-Force</span><span class="sxs-lookup"><span data-stu-id="292f4-135">-Force</span></span>
<span data-ttu-id="292f4-136">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="292f4-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="292f4-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="292f4-137">-OutputArchivePath</span></span>
<span data-ttu-id="292f4-138">Specifica il percorso di un file ZIP locale in cui scrivere l'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="292f4-139">Quando si usa questo parametro, lo script di configurazione non viene caricato nell'archivio BLOB di Azure.</span><span class="sxs-lookup"><span data-stu-id="292f4-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

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

### <span data-ttu-id="292f4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="292f4-140">-ResourceGroupName</span></span>
<span data-ttu-id="292f4-141">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-141">Specifies the name of the resource group that contains the storage account.</span></span>

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

### <span data-ttu-id="292f4-142">-SkipCtionyDetection</span><span class="sxs-lookup"><span data-stu-id="292f4-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="292f4-143">Indica che questo cmdlet esclude le dipendenze delle risorse DSC dall'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="292f4-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="292f4-144">-StorageAccountName</span></span>
<span data-ttu-id="292f4-145">Specifica il nome dell'account di archiviazione di Azure usato per caricare lo script di configurazione nel contenitore specificato dal *parametro ContainerName.*</span><span class="sxs-lookup"><span data-stu-id="292f4-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

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

### <span data-ttu-id="292f4-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="292f4-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="292f4-147">Specifica il suffisso per il punto finale di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="292f4-147">Specifies the suffix for the storage end point.</span></span>

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

### <span data-ttu-id="292f4-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="292f4-148">-Confirm</span></span>
<span data-ttu-id="292f4-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="292f4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="292f4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="292f4-150">-WhatIf</span></span>
<span data-ttu-id="292f4-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="292f4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="292f4-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="292f4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="292f4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292f4-153">CommonParameters</span></span>
<span data-ttu-id="292f4-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292f4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292f4-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="292f4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292f4-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="292f4-156">INPUTS</span></span>

### <span data-ttu-id="292f4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="292f4-157">System.String</span></span>

### <span data-ttu-id="292f4-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="292f4-158">System.String[]</span></span>

## <span data-ttu-id="292f4-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="292f4-159">OUTPUTS</span></span>

### <span data-ttu-id="292f4-160">System.String</span><span class="sxs-lookup"><span data-stu-id="292f4-160">System.String</span></span>

## <span data-ttu-id="292f4-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="292f4-161">NOTES</span></span>

## <span data-ttu-id="292f4-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="292f4-162">RELATED LINKS</span></span>

[<span data-ttu-id="292f4-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="292f4-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="292f4-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="292f4-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="292f4-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="292f4-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


