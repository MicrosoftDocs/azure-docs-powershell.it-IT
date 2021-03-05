---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: e5cef84d4ae45e4ce55b1f377ab16edc2449c72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962046"
---
# <span data-ttu-id="87a84-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="87a84-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="87a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a84-102">SYNOPSIS</span></span>
<span data-ttu-id="87a84-103">Ottenere un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="87a84-103">Get an application group.</span></span>

## <span data-ttu-id="87a84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87a84-104">SYNTAX</span></span>

### <span data-ttu-id="87a84-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87a84-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="87a84-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="87a84-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="87a84-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="87a84-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="87a84-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="87a84-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="87a84-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="87a84-109">DESCRIPTION</span></span>
<span data-ttu-id="87a84-110">Ottenere un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="87a84-110">Get an application group.</span></span>

## <span data-ttu-id="87a84-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87a84-111">EXAMPLES</span></span>

### <span data-ttu-id="87a84-112">Esempio 1: Ottenere un applicationGroup di Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="87a84-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="87a84-113">Questo comando ottiene un gruppo di risorse di Desktop virtuale Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87a84-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="87a84-114">Esempio 2: Elencare Gruppi Applicazioni Desktop virtuale Windows</span><span class="sxs-lookup"><span data-stu-id="87a84-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="87a84-115">Questo comando elenca un gruppo di risorse di Desktop virtuale Di Windows.</span><span class="sxs-lookup"><span data-stu-id="87a84-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="87a84-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87a84-116">PARAMETERS</span></span>

### <span data-ttu-id="87a84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a84-117">-DefaultProfile</span></span>
<span data-ttu-id="87a84-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87a84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a84-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="87a84-119">-Filter</span></span>
<span data-ttu-id="87a84-120">Espressione di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="87a84-120">OData filter expression.</span></span>
<span data-ttu-id="87a84-121">Le proprietà valide per il filtro sono applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="87a84-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a84-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87a84-122">-InputObject</span></span>
<span data-ttu-id="87a84-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="87a84-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87a84-124">-Name</span><span class="sxs-lookup"><span data-stu-id="87a84-124">-Name</span></span>
<span data-ttu-id="87a84-125">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="87a84-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a84-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a84-126">-ResourceGroupName</span></span>
<span data-ttu-id="87a84-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87a84-127">The name of the resource group.</span></span>
<span data-ttu-id="87a84-128">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="87a84-128">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a84-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87a84-129">-SubscriptionId</span></span>
<span data-ttu-id="87a84-130">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="87a84-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a84-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a84-131">CommonParameters</span></span>
<span data-ttu-id="87a84-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a84-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a84-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87a84-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a84-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="87a84-134">INPUTS</span></span>

### <span data-ttu-id="87a84-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="87a84-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="87a84-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87a84-136">OUTPUTS</span></span>

### <span data-ttu-id="87a84-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="87a84-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="87a84-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="87a84-138">NOTES</span></span>

<span data-ttu-id="87a84-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="87a84-139">ALIASES</span></span>

<span data-ttu-id="87a84-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="87a84-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87a84-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="87a84-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87a84-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87a84-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87a84-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="87a84-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87a84-144">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="87a84-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="87a84-145">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="87a84-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="87a84-146">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="87a84-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="87a84-147">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="87a84-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="87a84-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="87a84-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87a84-149">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="87a84-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="87a84-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87a84-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="87a84-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="87a84-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="87a84-152">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="87a84-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="87a84-153">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="87a84-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="87a84-154">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="87a84-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="87a84-155">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="87a84-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="87a84-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87a84-156">RELATED LINKS</span></span>

