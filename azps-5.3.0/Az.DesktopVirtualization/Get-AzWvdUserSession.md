---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 8dde4305003b97bd186a4601106a93e6f471edf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476379"
---
# <span data-ttu-id="275ea-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="275ea-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="275ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="275ea-102">SYNOPSIS</span></span>
<span data-ttu-id="275ea-103">Ottenere un userSession.</span><span class="sxs-lookup"><span data-stu-id="275ea-103">Get a userSession.</span></span>

## <span data-ttu-id="275ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="275ea-104">SYNTAX</span></span>

### <span data-ttu-id="275ea-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="275ea-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="275ea-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="275ea-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="275ea-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="275ea-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="275ea-108">List1</span><span class="sxs-lookup"><span data-stu-id="275ea-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="275ea-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="275ea-109">DESCRIPTION</span></span>
<span data-ttu-id="275ea-110">Ottenere un userSession.</span><span class="sxs-lookup"><span data-stu-id="275ea-110">Get a userSession.</span></span>

## <span data-ttu-id="275ea-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="275ea-111">EXAMPLES</span></span>

### <span data-ttu-id="275ea-112">Esempio 1: ottenere un desktop virtuale di Windows UserSession per nome</span><span class="sxs-lookup"><span data-stu-id="275ea-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="275ea-113">Questo comando consente di ottenere un UserSession desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="275ea-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="275ea-114">Esempio 2: elenco di Windows Virtual Desktop UserSessions</span><span class="sxs-lookup"><span data-stu-id="275ea-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="275ea-115">Questo comando elenca un UserSessions desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="275ea-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="275ea-116">Esempio 3: elenco di UserSessions desktop virtuali di Windows nel pool host</span><span class="sxs-lookup"><span data-stu-id="275ea-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="275ea-117">Questo comando elenca un UserSessions desktop virtuale di Windows in un host di sessione in un pool host.</span><span class="sxs-lookup"><span data-stu-id="275ea-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="275ea-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="275ea-118">PARAMETERS</span></span>

### <span data-ttu-id="275ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275ea-119">-DefaultProfile</span></span>
<span data-ttu-id="275ea-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="275ea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275ea-121">-Filtro</span><span class="sxs-lookup"><span data-stu-id="275ea-121">-Filter</span></span>
<span data-ttu-id="275ea-122">Espressione di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="275ea-122">OData filter expression.</span></span>
<span data-ttu-id="275ea-123">Le proprietà valide per il filtro sono userPrincipalName e SessionState.</span><span class="sxs-lookup"><span data-stu-id="275ea-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ea-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="275ea-124">-HostPoolName</span></span>
<span data-ttu-id="275ea-125">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ea-126">-ID</span><span class="sxs-lookup"><span data-stu-id="275ea-126">-Id</span></span>
<span data-ttu-id="275ea-127">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ea-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="275ea-128">-InputObject</span></span>
<span data-ttu-id="275ea-129">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="275ea-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="275ea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275ea-130">-ResourceGroupName</span></span>
<span data-ttu-id="275ea-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="275ea-131">The name of the resource group.</span></span>
<span data-ttu-id="275ea-132">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="275ea-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ea-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="275ea-133">-SessionHostName</span></span>
<span data-ttu-id="275ea-134">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275ea-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="275ea-135">-SubscriptionId</span></span>
<span data-ttu-id="275ea-136">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="275ea-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="275ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275ea-137">CommonParameters</span></span>
<span data-ttu-id="275ea-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275ea-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="275ea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275ea-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="275ea-140">INPUTS</span></span>

### <span data-ttu-id="275ea-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="275ea-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="275ea-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="275ea-142">OUTPUTS</span></span>

### <span data-ttu-id="275ea-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="275ea-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="275ea-144">Note</span><span class="sxs-lookup"><span data-stu-id="275ea-144">NOTES</span></span>

<span data-ttu-id="275ea-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="275ea-145">ALIASES</span></span>

<span data-ttu-id="275ea-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="275ea-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="275ea-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="275ea-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="275ea-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="275ea-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="275ea-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="275ea-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="275ea-150">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="275ea-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="275ea-151">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="275ea-152">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="275ea-153">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="275ea-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="275ea-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="275ea-155">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="275ea-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="275ea-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="275ea-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="275ea-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="275ea-158">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="275ea-159">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="275ea-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="275ea-160">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="275ea-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="275ea-161">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="275ea-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="275ea-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="275ea-162">RELATED LINKS</span></span>

