---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033132"
---
# <span data-ttu-id="47ea3-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="47ea3-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="47ea3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="47ea3-103">Ottenere un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="47ea3-103">Get a session host.</span></span>

## <span data-ttu-id="47ea3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47ea3-104">SYNTAX</span></span>

### <span data-ttu-id="47ea3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47ea3-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47ea3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="47ea3-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47ea3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47ea3-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="47ea3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47ea3-108">DESCRIPTION</span></span>
<span data-ttu-id="47ea3-109">Ottenere un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="47ea3-109">Get a session host.</span></span>

## <span data-ttu-id="47ea3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47ea3-110">EXAMPLES</span></span>

### <span data-ttu-id="47ea3-111">Esempio 1: ottenere un desktop virtuale di Windows SessionHost per nome</span><span class="sxs-lookup"><span data-stu-id="47ea3-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="47ea3-112">Questo comando consente di ottenere un SessionHost desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="47ea3-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="47ea3-113">Esempio 2: elenco di Windows Virtual Desktop SessionHosts</span><span class="sxs-lookup"><span data-stu-id="47ea3-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="47ea3-114">Questo comando elenca un SessionHosts desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="47ea3-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="47ea3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47ea3-115">PARAMETERS</span></span>

### <span data-ttu-id="47ea3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ea3-116">-DefaultProfile</span></span>
<span data-ttu-id="47ea3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47ea3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ea3-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="47ea3-118">-HostPoolName</span></span>
<span data-ttu-id="47ea3-119">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="47ea3-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="47ea3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47ea3-120">-InputObject</span></span>
<span data-ttu-id="47ea3-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="47ea3-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47ea3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="47ea3-122">-Name</span></span>
<span data-ttu-id="47ea3-123">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="47ea3-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ea3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ea3-124">-ResourceGroupName</span></span>
<span data-ttu-id="47ea3-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47ea3-125">The name of the resource group.</span></span>
<span data-ttu-id="47ea3-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="47ea3-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="47ea3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47ea3-127">-SubscriptionId</span></span>
<span data-ttu-id="47ea3-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="47ea3-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="47ea3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ea3-129">CommonParameters</span></span>
<span data-ttu-id="47ea3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ea3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ea3-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47ea3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ea3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47ea3-132">INPUTS</span></span>

### <span data-ttu-id="47ea3-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="47ea3-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="47ea3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47ea3-134">OUTPUTS</span></span>

### <span data-ttu-id="47ea3-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="47ea3-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="47ea3-136">Note</span><span class="sxs-lookup"><span data-stu-id="47ea3-136">NOTES</span></span>

<span data-ttu-id="47ea3-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="47ea3-137">ALIASES</span></span>

<span data-ttu-id="47ea3-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47ea3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47ea3-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="47ea3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47ea3-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47ea3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47ea3-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="47ea3-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47ea3-142">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="47ea3-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="47ea3-143">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="47ea3-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="47ea3-144">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="47ea3-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="47ea3-145">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="47ea3-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="47ea3-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="47ea3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47ea3-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47ea3-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="47ea3-148">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="47ea3-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="47ea3-149">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="47ea3-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="47ea3-150">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="47ea3-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="47ea3-151">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="47ea3-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="47ea3-152">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="47ea3-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="47ea3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47ea3-153">RELATED LINKS</span></span>

