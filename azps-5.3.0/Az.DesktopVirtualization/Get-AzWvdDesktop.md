---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: de52995d5cda17e332c137966f58b349d64c01f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475372"
---
# <span data-ttu-id="26440-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="26440-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="26440-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26440-102">SYNOPSIS</span></span>
<span data-ttu-id="26440-103">Ottenere un desktop.</span><span class="sxs-lookup"><span data-stu-id="26440-103">Get a desktop.</span></span>

## <span data-ttu-id="26440-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26440-104">SYNTAX</span></span>

### <span data-ttu-id="26440-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26440-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26440-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="26440-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26440-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26440-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="26440-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26440-108">DESCRIPTION</span></span>
<span data-ttu-id="26440-109">Ottenere un desktop.</span><span class="sxs-lookup"><span data-stu-id="26440-109">Get a desktop.</span></span>

## <span data-ttu-id="26440-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26440-110">EXAMPLES</span></span>

### <span data-ttu-id="26440-111">Esempio 1: ottenere un desktop di Windows Virtual Desktop per nome</span><span class="sxs-lookup"><span data-stu-id="26440-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="26440-112">Questo comando consente di ottenere un desktop desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="26440-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="26440-113">Esempio 2: elencare desktop desktop virtuali di Windows</span><span class="sxs-lookup"><span data-stu-id="26440-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="26440-114">Questo comando listsWindows desktop desktop virtuali in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="26440-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="26440-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26440-115">PARAMETERS</span></span>

### <span data-ttu-id="26440-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="26440-116">-ApplicationGroupName</span></span>
<span data-ttu-id="26440-117">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="26440-117">The name of the application group</span></span>

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

### <span data-ttu-id="26440-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26440-118">-DefaultProfile</span></span>
<span data-ttu-id="26440-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26440-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26440-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26440-120">-InputObject</span></span>
<span data-ttu-id="26440-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="26440-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="26440-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="26440-122">-Name</span></span>
<span data-ttu-id="26440-123">Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="26440-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26440-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26440-124">-ResourceGroupName</span></span>
<span data-ttu-id="26440-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26440-125">The name of the resource group.</span></span>
<span data-ttu-id="26440-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="26440-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="26440-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26440-127">-SubscriptionId</span></span>
<span data-ttu-id="26440-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26440-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26440-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26440-129">CommonParameters</span></span>
<span data-ttu-id="26440-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26440-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26440-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26440-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26440-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26440-132">INPUTS</span></span>

### <span data-ttu-id="26440-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="26440-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="26440-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26440-134">OUTPUTS</span></span>

### <span data-ttu-id="26440-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="26440-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="26440-136">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="26440-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="26440-137">Note</span><span class="sxs-lookup"><span data-stu-id="26440-137">NOTES</span></span>

<span data-ttu-id="26440-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="26440-138">ALIASES</span></span>

<span data-ttu-id="26440-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26440-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26440-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="26440-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26440-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26440-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26440-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="26440-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26440-143">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="26440-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="26440-144">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="26440-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="26440-145">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="26440-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="26440-146">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="26440-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="26440-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="26440-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26440-148">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="26440-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="26440-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26440-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="26440-150">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="26440-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="26440-151">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="26440-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="26440-152">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26440-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="26440-153">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="26440-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="26440-154">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="26440-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="26440-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26440-155">RELATED LINKS</span></span>

