---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209346"
---
# <span data-ttu-id="e0c25-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="e0c25-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="e0c25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c25-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c25-103">Restituisce i dettagli su una posizione a cui è possibile spedire i dischi associati a un processo di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="e0c25-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="e0c25-104">Una posizione è un'area geografica azure.</span><span class="sxs-lookup"><span data-stu-id="e0c25-104">A location is an Azure region.</span></span>

## <span data-ttu-id="e0c25-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0c25-105">SYNTAX</span></span>

### <span data-ttu-id="e0c25-106">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0c25-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0c25-107">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e0c25-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0c25-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0c25-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e0c25-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0c25-109">DESCRIPTION</span></span>
<span data-ttu-id="e0c25-110">Restituisce i dettagli su una posizione a cui è possibile spedire i dischi associati a un processo di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="e0c25-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="e0c25-111">Una posizione è un'area geografica azure.</span><span class="sxs-lookup"><span data-stu-id="e0c25-111">A location is an Azure region.</span></span>

## <span data-ttu-id="e0c25-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0c25-112">EXAMPLES</span></span>

### <span data-ttu-id="e0c25-113">Esempio 1: Ottenere tutti i dettagli sulla posizione dell'area geografica di Azure con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="e0c25-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="e0c25-114">Questo cmdlet ottiene tutti i dettagli sulla posizione dell'area geografica di Azure con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="e0c25-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="e0c25-115">Esempio 2: Ottenere i dettagli sulla posizione dell'area geografica di Azure in base al nome della posizione</span><span class="sxs-lookup"><span data-stu-id="e0c25-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="e0c25-116">Questo cmdlet recupera i dettagli sulla posizione dell'area geografica di Azure in base al nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e0c25-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="e0c25-117">Esempio 3: Ottenere i dettagli sulla posizione dell'area geografica di Azure in base all'identità</span><span class="sxs-lookup"><span data-stu-id="e0c25-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="e0c25-118">Questo elenco di cmdlet ottiene i dettagli sulla posizione dell'area geografica di Azure in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="e0c25-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="e0c25-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0c25-119">PARAMETERS</span></span>

### <span data-ttu-id="e0c25-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e0c25-120">-AcceptLanguage</span></span>
<span data-ttu-id="e0c25-121">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="e0c25-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="e0c25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c25-122">-DefaultProfile</span></span>
<span data-ttu-id="e0c25-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0c25-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c25-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0c25-124">-InputObject</span></span>
<span data-ttu-id="e0c25-125">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e0c25-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c25-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e0c25-126">-Name</span></span>
<span data-ttu-id="e0c25-127">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e0c25-127">The name of the location.</span></span>
<span data-ttu-id="e0c25-128">Ad esempio, Stati Uniti occidentali o Ovest.</span><span class="sxs-lookup"><span data-stu-id="e0c25-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0c25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c25-129">CommonParameters</span></span>
<span data-ttu-id="e0c25-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c25-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e0c25-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c25-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0c25-132">INPUTS</span></span>

### <span data-ttu-id="e0c25-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="e0c25-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="e0c25-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0c25-134">OUTPUTS</span></span>

### <span data-ttu-id="e0c25-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="e0c25-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="e0c25-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0c25-136">NOTES</span></span>

<span data-ttu-id="e0c25-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e0c25-137">ALIASES</span></span>

<span data-ttu-id="e0c25-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e0c25-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0c25-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e0c25-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0c25-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0c25-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0c25-141">INPUTOBJECT <IImportExportIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="e0c25-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0c25-142">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e0c25-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0c25-143">`[JobName <String>]`: nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="e0c25-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="e0c25-144">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e0c25-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="e0c25-145">Ad esempio, Stati Uniti occidentali o Ovest.</span><span class="sxs-lookup"><span data-stu-id="e0c25-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="e0c25-146">`[ResourceGroupName <String>]`: il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0c25-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="e0c25-147">`[SubscriptionId <String>]`: ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0c25-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="e0c25-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0c25-148">RELATED LINKS</span></span>

