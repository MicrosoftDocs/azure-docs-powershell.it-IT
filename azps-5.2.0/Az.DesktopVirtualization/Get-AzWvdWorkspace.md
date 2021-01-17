---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: b17fedefcac1acd260f9b3f0cf8834605a590ca9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369456"
---
# <span data-ttu-id="b6e2a-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6e2a-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="b6e2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e2a-103">Ottenere un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-103">Get a workspace.</span></span>

## <span data-ttu-id="b6e2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6e2a-104">SYNTAX</span></span>

### <span data-ttu-id="b6e2a-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6e2a-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6e2a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b6e2a-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6e2a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6e2a-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6e2a-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="b6e2a-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6e2a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6e2a-109">DESCRIPTION</span></span>
<span data-ttu-id="b6e2a-110">Ottenere un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-110">Get a workspace.</span></span>

## <span data-ttu-id="b6e2a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6e2a-111">EXAMPLES</span></span>

### <span data-ttu-id="b6e2a-112">Esempio 1: ottenere un'area di lavoro desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="b6e2a-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="b6e2a-113">Questo comando consente di ottenere un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="b6e2a-114">Esempio 2: elencare le aree di lavoro desktop virtuali di Windows</span><span class="sxs-lookup"><span data-stu-id="b6e2a-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="b6e2a-115">Questo comando elenca un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="b6e2a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6e2a-116">PARAMETERS</span></span>

### <span data-ttu-id="b6e2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e2a-117">-DefaultProfile</span></span>
<span data-ttu-id="b6e2a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e2a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6e2a-119">-InputObject</span></span>
<span data-ttu-id="b6e2a-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6e2a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6e2a-121">-Name</span></span>
<span data-ttu-id="b6e2a-122">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b6e2a-122">The name of the workspace</span></span>

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

### <span data-ttu-id="b6e2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6e2a-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-124">The name of the resource group.</span></span>
<span data-ttu-id="b6e2a-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b6e2a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6e2a-126">-SubscriptionId</span></span>
<span data-ttu-id="b6e2a-127">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b6e2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e2a-128">CommonParameters</span></span>
<span data-ttu-id="b6e2a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e2a-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e2a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6e2a-131">INPUTS</span></span>

### <span data-ttu-id="b6e2a-132">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b6e2a-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b6e2a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6e2a-133">OUTPUTS</span></span>

### <span data-ttu-id="b6e2a-134">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6e2a-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="b6e2a-135">Note</span><span class="sxs-lookup"><span data-stu-id="b6e2a-135">NOTES</span></span>

<span data-ttu-id="b6e2a-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b6e2a-136">ALIASES</span></span>

<span data-ttu-id="b6e2a-137">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6e2a-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6e2a-138">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6e2a-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6e2a-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b6e2a-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6e2a-141">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="b6e2a-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b6e2a-142">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="b6e2a-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b6e2a-143">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="b6e2a-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b6e2a-144">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="b6e2a-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b6e2a-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b6e2a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6e2a-146">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="b6e2a-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b6e2a-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b6e2a-148">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="b6e2a-149">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="b6e2a-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b6e2a-150">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b6e2a-151">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="b6e2a-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b6e2a-152">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b6e2a-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b6e2a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6e2a-153">RELATED LINKS</span></span>

