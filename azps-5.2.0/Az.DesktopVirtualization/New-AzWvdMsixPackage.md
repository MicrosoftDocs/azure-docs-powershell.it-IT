---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357615"
---
# <span data-ttu-id="20435-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="20435-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="20435-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20435-102">SYNOPSIS</span></span>
<span data-ttu-id="20435-103">Creare o aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="20435-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="20435-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20435-104">SYNTAX</span></span>

### <span data-ttu-id="20435-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20435-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="20435-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="20435-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="20435-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20435-107">DESCRIPTION</span></span>
<span data-ttu-id="20435-108">Creare o aggiornare un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="20435-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="20435-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20435-109">EXAMPLES</span></span>

### <span data-ttu-id="20435-110">Esempio 1: crea un nuovo pacchetto MSIX nell'alias HostPool tramite pacchetto</span><span class="sxs-lookup"><span data-stu-id="20435-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="20435-111">Questo comando aggiunge il pacchetto MSIX dal percorso immagine specificato a HostPool</span><span class="sxs-lookup"><span data-stu-id="20435-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="20435-112">Esempio 2: crea un nuovo pacchetto di MSIX in HostPool</span><span class="sxs-lookup"><span data-stu-id="20435-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="20435-113">Questo comando aggiunge il pacchetto MSIX nel HostPool specificato</span><span class="sxs-lookup"><span data-stu-id="20435-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="20435-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20435-114">PARAMETERS</span></span>

### <span data-ttu-id="20435-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20435-115">-DefaultProfile</span></span>
<span data-ttu-id="20435-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20435-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20435-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="20435-117">-DisplayName</span></span>
<span data-ttu-id="20435-118">Nome descrittivo dell'utente da visualizzare nel portale.</span><span class="sxs-lookup"><span data-stu-id="20435-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="20435-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="20435-119">-FullName</span></span>
<span data-ttu-id="20435-120">Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="20435-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="20435-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="20435-121">-HostPoolName</span></span>
<span data-ttu-id="20435-122">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="20435-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="20435-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="20435-123">-ImagePath</span></span>
<span data-ttu-id="20435-124">Percorso immagine VHD/CIM in condivisione di rete.</span><span class="sxs-lookup"><span data-stu-id="20435-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="20435-125">-Attiva</span><span class="sxs-lookup"><span data-stu-id="20435-125">-IsActive</span></span>
<span data-ttu-id="20435-126">Imposta questa versione del pacchetto su quella attiva in hostpool.</span><span class="sxs-lookup"><span data-stu-id="20435-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="20435-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="20435-127">-IsRegularRegistration</span></span>
<span data-ttu-id="20435-128">Specifica come registrare il pacchetto nel feed.</span><span class="sxs-lookup"><span data-stu-id="20435-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="20435-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="20435-129">-LastUpdated</span></span>
<span data-ttu-id="20435-130">Il pacchetto Data è stato aggiornato per ultimo, disponibile nel appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="20435-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="20435-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="20435-131">-PackageAlias</span></span>
<span data-ttu-id="20435-132">Pacchetto alias from Extract MSIX image</span><span class="sxs-lookup"><span data-stu-id="20435-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="20435-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="20435-133">-PackageApplication</span></span>
<span data-ttu-id="20435-134">Elenco delle applicazioni di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="20435-134">List of package applications.</span></span>

<span data-ttu-id="20435-135">Per costruire, vedere la sezione Note per le proprietà di PACKAGEAPPLICATION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="20435-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20435-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="20435-136">-PackageDependency</span></span>
<span data-ttu-id="20435-137">Elenco delle dipendenze del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="20435-137">List of package dependencies.</span></span>

<span data-ttu-id="20435-138">Per costruire, vedere la sezione Note per le proprietà di PACKAGEDEPENDENCY e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="20435-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20435-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="20435-139">-PackageFamilyName</span></span>
<span data-ttu-id="20435-140">Nome della famiglia di pacchetti da appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="20435-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="20435-141">Contiene il nome del pacchetto e il nome dell'editore.</span><span class="sxs-lookup"><span data-stu-id="20435-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="20435-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="20435-142">-PackageName</span></span>
<span data-ttu-id="20435-143">Nome pacchetto da appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="20435-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="20435-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="20435-144">-PackageRelativePath</span></span>
<span data-ttu-id="20435-145">Percorso relativo al pacchetto all'interno dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="20435-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="20435-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20435-146">-ResourceGroupName</span></span>
<span data-ttu-id="20435-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20435-147">The name of the resource group.</span></span>
<span data-ttu-id="20435-148">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="20435-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="20435-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20435-149">-SubscriptionId</span></span>
<span data-ttu-id="20435-150">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="20435-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="20435-151">-Versione</span><span class="sxs-lookup"><span data-stu-id="20435-151">-Version</span></span>
<span data-ttu-id="20435-152">Versione del pacchetto trovata nel appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="20435-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="20435-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="20435-153">-Confirm</span></span>
<span data-ttu-id="20435-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20435-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20435-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20435-155">-WhatIf</span></span>
<span data-ttu-id="20435-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20435-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20435-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20435-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20435-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20435-158">CommonParameters</span></span>
<span data-ttu-id="20435-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20435-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20435-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20435-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20435-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20435-161">INPUTS</span></span>

## <span data-ttu-id="20435-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20435-162">OUTPUTS</span></span>

### <span data-ttu-id="20435-163">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="20435-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="20435-164">Note</span><span class="sxs-lookup"><span data-stu-id="20435-164">NOTES</span></span>

<span data-ttu-id="20435-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="20435-165">ALIASES</span></span>

<span data-ttu-id="20435-166">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20435-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20435-167">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="20435-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20435-168">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20435-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20435-169">PACKAGEAPPLICATION <IMsixPackageApplications [] >: elenco delle applicazioni di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="20435-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="20435-170">`[AppId <String>]`: ID applicazione pacchetto, disponibile in appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="20435-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="20435-171">`[AppUserModelId <String>]`: Usato per attivare l'applicazione pacchetto.</span><span class="sxs-lookup"><span data-stu-id="20435-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="20435-172">È costituito dal nome del pacchetto e ApplicationID.</span><span class="sxs-lookup"><span data-stu-id="20435-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="20435-173">Disponibile in appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="20435-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="20435-174">`[Description <String>]`: Descrizione dell'applicazione pacchetto.</span><span class="sxs-lookup"><span data-stu-id="20435-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="20435-175">`[FriendlyName <String>]`: Nome descrittivo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="20435-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="20435-176">`[IconImageName <String>]`: Nome descrittivo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="20435-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="20435-177">`[RawIcon <Byte[]>]`: l'icona una stringa di bit di 64 come matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="20435-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="20435-178">`[RawPng <Byte[]>]`: l'icona una stringa di bit di 64 come matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="20435-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="20435-179">PACKAGEDEPENDENCY <IMsixPackageDependencies [] >: elenco delle dipendenze del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="20435-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="20435-180">`[DependencyName <String>]`: Nome della dipendenza del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="20435-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="20435-181">`[MinVersion <String>]`: È necessaria la versione di dipendenza.</span><span class="sxs-lookup"><span data-stu-id="20435-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="20435-182">`[Publisher <String>]`: Nome dell'autore della dipendenza.</span><span class="sxs-lookup"><span data-stu-id="20435-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="20435-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20435-183">RELATED LINKS</span></span>

