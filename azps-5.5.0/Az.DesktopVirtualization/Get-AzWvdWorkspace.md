---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 3fa80fc69679346e3462a96340f4af9fc6a251d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186070"
---
# <span data-ttu-id="8be06-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="8be06-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="8be06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be06-102">SYNOPSIS</span></span>
<span data-ttu-id="8be06-103">Ottenere un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8be06-103">Get a workspace.</span></span>

## <span data-ttu-id="8be06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8be06-104">SYNTAX</span></span>

### <span data-ttu-id="8be06-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8be06-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8be06-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8be06-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8be06-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8be06-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8be06-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="8be06-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8be06-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8be06-109">DESCRIPTION</span></span>
<span data-ttu-id="8be06-110">Ottenere un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8be06-110">Get a workspace.</span></span>

## <span data-ttu-id="8be06-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8be06-111">EXAMPLES</span></span>

### <span data-ttu-id="8be06-112">Esempio 1: ottenere un'area di lavoro desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="8be06-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="8be06-113">Questo comando recupera un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8be06-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="8be06-114">Esempio 2: Elencare aree di lavoro desktop virtuale Windows</span><span class="sxs-lookup"><span data-stu-id="8be06-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="8be06-115">Questo comando elenca le aree di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8be06-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="8be06-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8be06-116">PARAMETERS</span></span>

### <span data-ttu-id="8be06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be06-117">-DefaultProfile</span></span>
<span data-ttu-id="8be06-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8be06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be06-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8be06-119">-InputObject</span></span>
<span data-ttu-id="8be06-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8be06-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8be06-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8be06-121">-Name</span></span>
<span data-ttu-id="8be06-122">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="8be06-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be06-123">-ResourceGroupName</span></span>
<span data-ttu-id="8be06-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8be06-124">The name of the resource group.</span></span>
<span data-ttu-id="8be06-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8be06-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8be06-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8be06-126">-SubscriptionId</span></span>
<span data-ttu-id="8be06-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8be06-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8be06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be06-128">CommonParameters</span></span>
<span data-ttu-id="8be06-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be06-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8be06-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be06-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="8be06-131">INPUTS</span></span>

### <span data-ttu-id="8be06-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8be06-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8be06-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8be06-133">OUTPUTS</span></span>

### <span data-ttu-id="8be06-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="8be06-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="8be06-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="8be06-135">NOTES</span></span>

<span data-ttu-id="8be06-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8be06-136">ALIASES</span></span>

<span data-ttu-id="8be06-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="8be06-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8be06-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8be06-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8be06-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8be06-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8be06-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="8be06-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8be06-141">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="8be06-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8be06-142">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="8be06-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8be06-143">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="8be06-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8be06-144">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="8be06-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8be06-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="8be06-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8be06-146">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="8be06-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8be06-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8be06-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8be06-148">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8be06-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="8be06-149">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="8be06-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8be06-150">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8be06-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8be06-151">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="8be06-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8be06-152">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="8be06-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8be06-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8be06-153">RELATED LINKS</span></span>

