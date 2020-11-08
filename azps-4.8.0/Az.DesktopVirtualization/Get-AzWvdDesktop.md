---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033133"
---
# <span data-ttu-id="af0c2-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="af0c2-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="af0c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="af0c2-103">Ottenere un desktop.</span><span class="sxs-lookup"><span data-stu-id="af0c2-103">Get a desktop.</span></span>

## <span data-ttu-id="af0c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af0c2-104">SYNTAX</span></span>

### <span data-ttu-id="af0c2-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af0c2-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="af0c2-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="af0c2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="af0c2-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="af0c2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af0c2-108">DESCRIPTION</span></span>
<span data-ttu-id="af0c2-109">Ottenere un desktop.</span><span class="sxs-lookup"><span data-stu-id="af0c2-109">Get a desktop.</span></span>

## <span data-ttu-id="af0c2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af0c2-110">EXAMPLES</span></span>

### <span data-ttu-id="af0c2-111">Esempio 1: ottenere un desktop di Windows Virtual Desktop per nome</span><span class="sxs-lookup"><span data-stu-id="af0c2-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="af0c2-112">Questo comando consente di ottenere un desktop desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="af0c2-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="af0c2-113">Esempio 2: elencare desktop desktop virtuali di Windows</span><span class="sxs-lookup"><span data-stu-id="af0c2-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="af0c2-114">Questo comando listsWindows desktop desktop virtuali in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="af0c2-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="af0c2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af0c2-115">PARAMETERS</span></span>

### <span data-ttu-id="af0c2-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="af0c2-116">-ApplicationGroupName</span></span>
<span data-ttu-id="af0c2-117">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="af0c2-117">The name of the application group</span></span>

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

### <span data-ttu-id="af0c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af0c2-118">-DefaultProfile</span></span>
<span data-ttu-id="af0c2-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af0c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af0c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af0c2-120">-InputObject</span></span>
<span data-ttu-id="af0c2-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="af0c2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="af0c2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="af0c2-122">-Name</span></span>
<span data-ttu-id="af0c2-123">Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="af0c2-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="af0c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af0c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="af0c2-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af0c2-125">The name of the resource group.</span></span>
<span data-ttu-id="af0c2-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="af0c2-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="af0c2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af0c2-127">-SubscriptionId</span></span>
<span data-ttu-id="af0c2-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af0c2-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="af0c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af0c2-129">CommonParameters</span></span>
<span data-ttu-id="af0c2-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af0c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af0c2-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af0c2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af0c2-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af0c2-132">INPUTS</span></span>

### <span data-ttu-id="af0c2-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="af0c2-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="af0c2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af0c2-134">OUTPUTS</span></span>

### <span data-ttu-id="af0c2-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="af0c2-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="af0c2-136">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="af0c2-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="af0c2-137">Note</span><span class="sxs-lookup"><span data-stu-id="af0c2-137">NOTES</span></span>

<span data-ttu-id="af0c2-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="af0c2-138">ALIASES</span></span>

<span data-ttu-id="af0c2-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af0c2-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af0c2-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="af0c2-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af0c2-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af0c2-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af0c2-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="af0c2-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af0c2-143">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="af0c2-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="af0c2-144">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="af0c2-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="af0c2-145">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="af0c2-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="af0c2-146">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="af0c2-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="af0c2-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="af0c2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af0c2-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af0c2-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="af0c2-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="af0c2-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="af0c2-150">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="af0c2-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="af0c2-151">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af0c2-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="af0c2-152">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="af0c2-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="af0c2-153">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="af0c2-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="af0c2-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af0c2-154">RELATED LINKS</span></span>

