---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: a19d1e39fb9ef2e982b569b8c0351d8d1bde1fb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966174"
---
# <span data-ttu-id="b1f59-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="b1f59-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="b1f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1f59-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f59-103">Ottenere una userSession.</span><span class="sxs-lookup"><span data-stu-id="b1f59-103">Get a userSession.</span></span>

## <span data-ttu-id="b1f59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1f59-104">SYNTAX</span></span>

### <span data-ttu-id="b1f59-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1f59-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1f59-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b1f59-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1f59-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1f59-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1f59-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="b1f59-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b1f59-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1f59-109">DESCRIPTION</span></span>
<span data-ttu-id="b1f59-110">Ottenere una userSession.</span><span class="sxs-lookup"><span data-stu-id="b1f59-110">Get a userSession.</span></span>

## <span data-ttu-id="b1f59-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1f59-111">EXAMPLES</span></span>

### <span data-ttu-id="b1f59-112">Esempio 1: Ottenere un userSession di Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="b1f59-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="b1f59-113">Questo comando ottiene una UserSession di Desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="b1f59-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="b1f59-114">Esempio 2: Elencare le UserSessions di Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="b1f59-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="b1f59-115">Questo comando elenca le UserSessions di Desktop virtuale di Windows in un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="b1f59-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="b1f59-116">Esempio 3: Elencare le UserSessions di Desktop virtuale di Windows nel pool host</span><span class="sxs-lookup"><span data-stu-id="b1f59-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="b1f59-117">Questo comando elenca le UserSessions di Desktop virtuale di Windows in un host di sessione in un pool host.</span><span class="sxs-lookup"><span data-stu-id="b1f59-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="b1f59-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1f59-118">PARAMETERS</span></span>

### <span data-ttu-id="b1f59-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f59-119">-DefaultProfile</span></span>
<span data-ttu-id="b1f59-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f59-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f59-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="b1f59-121">-Filter</span></span>
<span data-ttu-id="b1f59-122">Espressione di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="b1f59-122">OData filter expression.</span></span>
<span data-ttu-id="b1f59-123">Le proprietà valide per il filtro sono userprincipalname e sessionstate.</span><span class="sxs-lookup"><span data-stu-id="b1f59-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="b1f59-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b1f59-124">-HostPoolName</span></span>
<span data-ttu-id="b1f59-125">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b1f59-126">-Id</span><span class="sxs-lookup"><span data-stu-id="b1f59-126">-Id</span></span>
<span data-ttu-id="b1f59-127">Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="b1f59-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1f59-128">-InputObject</span></span>
<span data-ttu-id="b1f59-129">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b1f59-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1f59-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f59-130">-ResourceGroupName</span></span>
<span data-ttu-id="b1f59-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1f59-131">The name of the resource group.</span></span>
<span data-ttu-id="b1f59-132">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b1f59-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b1f59-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="b1f59-133">-SessionHostName</span></span>
<span data-ttu-id="b1f59-134">Nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="b1f59-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1f59-135">-SubscriptionId</span></span>
<span data-ttu-id="b1f59-136">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b1f59-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b1f59-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f59-137">CommonParameters</span></span>
<span data-ttu-id="b1f59-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f59-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f59-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1f59-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f59-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1f59-140">INPUTS</span></span>

### <span data-ttu-id="b1f59-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b1f59-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b1f59-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1f59-142">OUTPUTS</span></span>

### <span data-ttu-id="b1f59-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="b1f59-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="b1f59-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1f59-144">NOTES</span></span>

<span data-ttu-id="b1f59-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b1f59-145">ALIASES</span></span>

<span data-ttu-id="b1f59-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b1f59-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1f59-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b1f59-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1f59-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1f59-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1f59-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b1f59-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1f59-150">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="b1f59-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b1f59-151">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b1f59-152">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b1f59-153">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b1f59-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b1f59-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1f59-155">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b1f59-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1f59-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b1f59-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b1f59-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="b1f59-158">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b1f59-159">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b1f59-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b1f59-160">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="b1f59-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b1f59-161">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b1f59-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b1f59-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1f59-162">RELATED LINKS</span></span>

