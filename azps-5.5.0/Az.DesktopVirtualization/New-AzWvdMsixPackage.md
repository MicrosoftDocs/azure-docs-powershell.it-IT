---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: 162071e07e8081f80e4187f049aef8931dcffc78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196438"
---
# <span data-ttu-id="eb59e-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="eb59e-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="eb59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb59e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb59e-103">Creare o aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="eb59e-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="eb59e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb59e-104">SYNTAX</span></span>

### <span data-ttu-id="eb59e-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb59e-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eb59e-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="eb59e-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eb59e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eb59e-107">DESCRIPTION</span></span>
<span data-ttu-id="eb59e-108">Creare o aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="eb59e-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="eb59e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb59e-109">EXAMPLES</span></span>

### <span data-ttu-id="eb59e-110">Esempio 1: Crea un nuovo pacchetto MSIX in HostPool tramite alias del pacchetto</span><span class="sxs-lookup"><span data-stu-id="eb59e-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="eb59e-111">Questo comando aggiunge il pacchetto MSIX dal percorso immagine specificato a HostPool</span><span class="sxs-lookup"><span data-stu-id="eb59e-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="eb59e-112">Esempio 2: Crea un nuovo pacchetto MSIX nell'hostPool</span><span class="sxs-lookup"><span data-stu-id="eb59e-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="eb59e-113">Questo comando aggiunge il pacchetto MSIX nell'hostPool specificato</span><span class="sxs-lookup"><span data-stu-id="eb59e-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="eb59e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb59e-114">PARAMETERS</span></span>

### <span data-ttu-id="eb59e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb59e-115">-DefaultProfile</span></span>
<span data-ttu-id="eb59e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb59e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb59e-117">-DisplayName</span></span>
<span data-ttu-id="eb59e-118">Nome descrittivo da visualizzare nel portale.</span><span class="sxs-lookup"><span data-stu-id="eb59e-118">User friendly Name to be displayed in the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="eb59e-119">-FullName</span></span>
<span data-ttu-id="eb59e-120">Nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="eb59e-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="eb59e-121">-HostPoolName</span></span>
<span data-ttu-id="eb59e-122">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="eb59e-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="eb59e-123">-ImagePath</span></span>
<span data-ttu-id="eb59e-124">Percorso immagine VHD/CIM in Condivisione di rete.</span><span class="sxs-lookup"><span data-stu-id="eb59e-124">VHD/CIM image path on Network Share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="eb59e-125">-IsActive</span></span>
<span data-ttu-id="eb59e-126">Impostare questa versione del pacchetto come attiva nell'hostpool.</span><span class="sxs-lookup"><span data-stu-id="eb59e-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="eb59e-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="eb59e-127">-IsRegularRegistration</span></span>
<span data-ttu-id="eb59e-128">Specifica come registrare il pacchetto nel feed.</span><span class="sxs-lookup"><span data-stu-id="eb59e-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="eb59e-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="eb59e-129">-LastUpdated</span></span>
<span data-ttu-id="eb59e-130">Data dell'ultimo aggiornamento del pacchetto, trovato nel appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="eb59e-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="eb59e-131">-PackageAlias</span></span>
<span data-ttu-id="eb59e-132">Package Alias from extract MSIX Image</span><span class="sxs-lookup"><span data-stu-id="eb59e-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="eb59e-133">-PackageApplication</span></span>
<span data-ttu-id="eb59e-134">Elenco di applicazioni di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="eb59e-134">List of package applications.</span></span>

<span data-ttu-id="eb59e-135">Per creare, vedere la sezione NOTE per le proprietà PACKAGEAPPLICATION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="eb59e-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-136">-Package Unise</span><span class="sxs-lookup"><span data-stu-id="eb59e-136">-PackageDependency</span></span>
<span data-ttu-id="eb59e-137">Elenco delle dipendenze dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="eb59e-137">List of package dependencies.</span></span>

<span data-ttu-id="eb59e-138">Per la costruzione, vedere la sezione NOTE per le proprietà PACKAGE PIÙ.SE E CREARE una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="eb59e-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="eb59e-139">-PackageFamilyName</span></span>
<span data-ttu-id="eb59e-140">Nome della famiglia di pacchetti appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="eb59e-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="eb59e-141">Contiene il nome del pacchetto e il nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="eb59e-141">Contains Package Name and Publisher name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="eb59e-142">-PackageName</span></span>
<span data-ttu-id="eb59e-143">Nome pacchetto da appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="eb59e-143">Package Name from appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="eb59e-144">-PackageRelativePath</span></span>
<span data-ttu-id="eb59e-145">Percorso relativo del pacchetto all'interno dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="eb59e-145">Relative Path to the package inside the image.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb59e-146">-ResourceGroupName</span></span>
<span data-ttu-id="eb59e-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb59e-147">The name of the resource group.</span></span>
<span data-ttu-id="eb59e-148">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="eb59e-148">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb59e-149">-SubscriptionId</span></span>
<span data-ttu-id="eb59e-150">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eb59e-150">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-151">-Version</span><span class="sxs-lookup"><span data-stu-id="eb59e-151">-Version</span></span>
<span data-ttu-id="eb59e-152">Package Version found in the appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="eb59e-152">Package Version found in the appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb59e-153">-Confirm</span></span>
<span data-ttu-id="eb59e-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb59e-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb59e-155">-WhatIf</span></span>
<span data-ttu-id="eb59e-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb59e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb59e-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb59e-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb59e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb59e-158">CommonParameters</span></span>
<span data-ttu-id="eb59e-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb59e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb59e-160">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb59e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb59e-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="eb59e-161">INPUTS</span></span>

## <span data-ttu-id="eb59e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb59e-162">OUTPUTS</span></span>

### <span data-ttu-id="eb59e-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="eb59e-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="eb59e-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="eb59e-164">NOTES</span></span>

<span data-ttu-id="eb59e-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eb59e-165">ALIASES</span></span>

<span data-ttu-id="eb59e-166">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="eb59e-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb59e-167">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="eb59e-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb59e-168">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb59e-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb59e-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: elenco di applicazioni di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="eb59e-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="eb59e-170">`[AppId <String>]`: ID pacchetto dell'applicazione trovato nel appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="eb59e-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="eb59e-171">`[AppUserModelId <String>]`: consente di attivare l'applicazione di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="eb59e-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="eb59e-172">È costituito dal nome del pacchetto e da ApplicationID.</span><span class="sxs-lookup"><span data-stu-id="eb59e-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="eb59e-173">Trovato in appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="eb59e-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="eb59e-174">`[Description <String>]`: Descrizione dell'applicazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="eb59e-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="eb59e-175">`[FriendlyName <String>]`: nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="eb59e-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="eb59e-176">`[IconImageName <String>]`: nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="eb59e-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="eb59e-177">`[RawIcon <Byte[]>]`: l'icona è una stringa a 64 bit come matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="eb59e-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="eb59e-178">`[RawPng <Byte[]>]`: l'icona è una stringa a 64 bit come matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="eb59e-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="eb59e-179">PACKAGE PIÙ.<IMsixPackage>: elenco delle dipendenze del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="eb59e-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="eb59e-180">`[DependencyName <String>]`: nome della dipendenza del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="eb59e-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="eb59e-181">`[MinVersion <String>]`: è necessaria la versione della dipendenza.</span><span class="sxs-lookup"><span data-stu-id="eb59e-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="eb59e-182">`[Publisher <String>]`: nome dell'autore della relazione.</span><span class="sxs-lookup"><span data-stu-id="eb59e-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="eb59e-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb59e-183">RELATED LINKS</span></span>

