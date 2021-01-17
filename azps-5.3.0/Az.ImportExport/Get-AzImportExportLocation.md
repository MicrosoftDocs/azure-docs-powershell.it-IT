---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487315"
---
# <span data-ttu-id="362e0-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="362e0-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="362e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="362e0-102">SYNOPSIS</span></span>
<span data-ttu-id="362e0-103">Restituisce i dettagli relativi a una posizione in cui è possibile spedire i dischi associati a un processo di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="362e0-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="362e0-104">Una posizione è un'area di Azure.</span><span class="sxs-lookup"><span data-stu-id="362e0-104">A location is an Azure region.</span></span>

## <span data-ttu-id="362e0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="362e0-105">SYNTAX</span></span>

### <span data-ttu-id="362e0-106">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="362e0-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="362e0-107">Ottieni</span><span class="sxs-lookup"><span data-stu-id="362e0-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="362e0-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="362e0-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="362e0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="362e0-109">DESCRIPTION</span></span>
<span data-ttu-id="362e0-110">Restituisce i dettagli relativi a una posizione in cui è possibile spedire i dischi associati a un processo di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="362e0-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="362e0-111">Una posizione è un'area di Azure.</span><span class="sxs-lookup"><span data-stu-id="362e0-111">A location is an Azure region.</span></span>

## <span data-ttu-id="362e0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="362e0-112">EXAMPLES</span></span>

### <span data-ttu-id="362e0-113">Esempio 1: ottenere tutti i dettagli della posizione dell'area di Azure con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="362e0-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="362e0-114">Questo cmdlet ottiene tutti i dettagli della posizione dell'area di Azure con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="362e0-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="362e0-115">Esempio 2: ottenere i dettagli della posizione dell'area di Azure in base al nome della posizione</span><span class="sxs-lookup"><span data-stu-id="362e0-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="362e0-116">Questo cmdlet ottiene i dettagli della posizione dell'area Azure in base al nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="362e0-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="362e0-117">Esempio 3: ottenere i dettagli della posizione dell'area geografica Azure per identità</span><span class="sxs-lookup"><span data-stu-id="362e0-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="362e0-118">Questo cmdlet elenca i dettagli della posizione dell'area di Azure in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="362e0-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="362e0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="362e0-119">PARAMETERS</span></span>

### <span data-ttu-id="362e0-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="362e0-120">-AcceptLanguage</span></span>
<span data-ttu-id="362e0-121">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="362e0-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="362e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362e0-122">-DefaultProfile</span></span>
<span data-ttu-id="362e0-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="362e0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="362e0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="362e0-124">-InputObject</span></span>
<span data-ttu-id="362e0-125">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="362e0-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="362e0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="362e0-126">-Name</span></span>
<span data-ttu-id="362e0-127">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="362e0-127">The name of the location.</span></span>
<span data-ttu-id="362e0-128">Ad esempio, ovest degli Stati Uniti o westus.</span><span class="sxs-lookup"><span data-stu-id="362e0-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="362e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362e0-129">CommonParameters</span></span>
<span data-ttu-id="362e0-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362e0-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="362e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362e0-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="362e0-132">INPUTS</span></span>

### <span data-ttu-id="362e0-133">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="362e0-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="362e0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="362e0-134">OUTPUTS</span></span>

### <span data-ttu-id="362e0-135">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="362e0-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="362e0-136">Note</span><span class="sxs-lookup"><span data-stu-id="362e0-136">NOTES</span></span>

<span data-ttu-id="362e0-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="362e0-137">ALIASES</span></span>

<span data-ttu-id="362e0-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="362e0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="362e0-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="362e0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="362e0-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="362e0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="362e0-141">INPUTOBJECT <IImportExportIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="362e0-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="362e0-142">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="362e0-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="362e0-143">`[JobName <String>]`: Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="362e0-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="362e0-144">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="362e0-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="362e0-145">Ad esempio, ovest degli Stati Uniti o westus.</span><span class="sxs-lookup"><span data-stu-id="362e0-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="362e0-146">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="362e0-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="362e0-147">`[SubscriptionId <String>]`: ID abbonamento per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="362e0-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="362e0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="362e0-148">RELATED LINKS</span></span>

