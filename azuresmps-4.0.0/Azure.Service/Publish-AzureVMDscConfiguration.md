---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023840"
---
# <span data-ttu-id="b1da2-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1da2-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="b1da2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1da2-102">SYNOPSIS</span></span>
<span data-ttu-id="b1da2-103">Pubblica uno script di configurazione dello stato desiderato in Azure BLOB Storage.</span><span class="sxs-lookup"><span data-stu-id="b1da2-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="b1da2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1da2-104">SYNTAX</span></span>

### <span data-ttu-id="b1da2-105">UploadArchive (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1da2-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1da2-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="b1da2-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1da2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1da2-107">DESCRIPTION</span></span>
<span data-ttu-id="b1da2-108">Il cmdlet **Publish-AzureVMDscConfiguration** pubblica uno script di configurazione dello stato desiderato in Azure BLOB Storage, che in seguito può essere applicato alle macchine virtuali di Azure usando il cmdlet **set-AzureVMDscExtension** .</span><span class="sxs-lookup"><span data-stu-id="b1da2-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="b1da2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1da2-109">EXAMPLES</span></span>

### <span data-ttu-id="b1da2-110">Esempio 1: pubblicare uno script di configurazione dello stato nell'archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="b1da2-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="b1da2-111">Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo carica in Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b1da2-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="b1da2-112">Esempio 2: pubblicare uno script di configurazione di stato in un file locale</span><span class="sxs-lookup"><span data-stu-id="b1da2-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="b1da2-113">Questo comando crea un pacchetto zip per lo script specifico e tutti i moduli di risorse dipendenti e lo archivia nel file locale .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="b1da2-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="b1da2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1da2-114">PARAMETERS</span></span>

### <span data-ttu-id="b1da2-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="b1da2-115">-AdditionalPath</span></span>
<span data-ttu-id="b1da2-116">Specifica una matrice di percorsi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b1da2-116">Specifies an array of additional paths.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="b1da2-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="b1da2-118">Specifica il percorso di un file con estensione zip locale che questo cmdlet scrive nell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b1da2-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="b1da2-119">Lo script di configurazione non viene caricato nell'archiviazione BLOB di Azure se si usa questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b1da2-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="b1da2-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="b1da2-121">Specifica un percorso di dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b1da2-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="b1da2-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="b1da2-122">-ConfigurationPath</span></span>
<span data-ttu-id="b1da2-123">Specifica il percorso di un file che contiene una o più configurazioni.</span><span class="sxs-lookup"><span data-stu-id="b1da2-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="b1da2-124">Il file può essere uno script di Windows PowerShell (file con estensione ps1), un modulo (file con estensione psm1) o un file di archivio (con estensione zip) che contiene un set di moduli di Windows PowerShell, con ogni modulo in una directory separata.</span><span class="sxs-lookup"><span data-stu-id="b1da2-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-125">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b1da2-125">-ContainerName</span></span>
<span data-ttu-id="b1da2-126">Specifica il nome del contenitore di archiviazione di Azure a cui è stata caricata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="b1da2-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b1da2-127">-Force</span></span>
<span data-ttu-id="b1da2-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b1da2-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1da2-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b1da2-129">-InformationAction</span></span>
<span data-ttu-id="b1da2-130">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b1da2-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b1da2-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1da2-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1da2-132">Continuare</span><span class="sxs-lookup"><span data-stu-id="b1da2-132">Continue</span></span>
- <span data-ttu-id="b1da2-133">Ignora</span><span class="sxs-lookup"><span data-stu-id="b1da2-133">Ignore</span></span>
- <span data-ttu-id="b1da2-134">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b1da2-134">Inquire</span></span>
- <span data-ttu-id="b1da2-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b1da2-135">SilentlyContinue</span></span>
- <span data-ttu-id="b1da2-136">Stop</span><span class="sxs-lookup"><span data-stu-id="b1da2-136">Stop</span></span>
- <span data-ttu-id="b1da2-137">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b1da2-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b1da2-138">-InformationVariable</span></span>
<span data-ttu-id="b1da2-139">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b1da2-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1da2-140">-PassThru</span></span>
<span data-ttu-id="b1da2-141">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b1da2-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1da2-142">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b1da2-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1da2-143">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1da2-143">-Profile</span></span>
<span data-ttu-id="b1da2-144">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1da2-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1da2-145">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b1da2-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1da2-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="b1da2-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="b1da2-147">Indica che questo cmdlet ignora il rilevamento delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="b1da2-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="b1da2-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b1da2-148">-StorageContext</span></span>
<span data-ttu-id="b1da2-149">Specifica il contesto di archiviazione di Azure che fornisce le impostazioni di sicurezza usate per caricare lo script di configurazione nel contenitore specificato dal parametro *containerName* .</span><span class="sxs-lookup"><span data-stu-id="b1da2-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="b1da2-150">Questo contesto fornisce l'accesso in scrittura al contenitore.</span><span class="sxs-lookup"><span data-stu-id="b1da2-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b1da2-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="b1da2-152">Specifica il suffisso per il punto finale dello spazio di archiviazione, ad esempio core.contoso.net</span><span class="sxs-lookup"><span data-stu-id="b1da2-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1da2-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1da2-153">-Confirm</span></span>
<span data-ttu-id="b1da2-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1da2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1da2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1da2-155">-WhatIf</span></span>
<span data-ttu-id="b1da2-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1da2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1da2-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1da2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1da2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1da2-158">CommonParameters</span></span>
<span data-ttu-id="b1da2-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1da2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1da2-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1da2-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1da2-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1da2-161">INPUTS</span></span>

## <span data-ttu-id="b1da2-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1da2-162">OUTPUTS</span></span>

## <span data-ttu-id="b1da2-163">Note</span><span class="sxs-lookup"><span data-stu-id="b1da2-163">NOTES</span></span>

## <span data-ttu-id="b1da2-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1da2-164">RELATED LINKS</span></span>

[<span data-ttu-id="b1da2-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b1da2-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


