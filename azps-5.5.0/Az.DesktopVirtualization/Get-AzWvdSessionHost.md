---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 462f49884a7e38ea6808b594b091a6cca94c4e5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180791"
---
# <span data-ttu-id="4e742-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="4e742-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="4e742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e742-102">SYNOPSIS</span></span>
<span data-ttu-id="4e742-103">Ottenere un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="4e742-103">Get a session host.</span></span>

## <span data-ttu-id="4e742-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e742-104">SYNTAX</span></span>

### <span data-ttu-id="4e742-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e742-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e742-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="4e742-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e742-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e742-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e742-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4e742-108">DESCRIPTION</span></span>
<span data-ttu-id="4e742-109">Ottenere un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="4e742-109">Get a session host.</span></span>

## <span data-ttu-id="4e742-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e742-110">EXAMPLES</span></span>

### <span data-ttu-id="4e742-111">Esempio 1: Ottenere un sessionHost di Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="4e742-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="4e742-112">Questo comando ottiene un sessionhost di Desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="4e742-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="4e742-113">Esempio 2: Elencare i sessionHost di Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="4e742-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="4e742-114">Questo comando elenca gli host di desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="4e742-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="4e742-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e742-115">PARAMETERS</span></span>

### <span data-ttu-id="4e742-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e742-116">-DefaultProfile</span></span>
<span data-ttu-id="4e742-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e742-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e742-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4e742-118">-HostPoolName</span></span>
<span data-ttu-id="4e742-119">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="4e742-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e742-120">-InputObject</span></span>
<span data-ttu-id="4e742-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4e742-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e742-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4e742-122">-Name</span></span>
<span data-ttu-id="4e742-123">Nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-123">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="4e742-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e742-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e742-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e742-125">The name of the resource group.</span></span>
<span data-ttu-id="4e742-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4e742-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4e742-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e742-127">-SubscriptionId</span></span>
<span data-ttu-id="4e742-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4e742-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4e742-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e742-129">CommonParameters</span></span>
<span data-ttu-id="4e742-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e742-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e742-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e742-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e742-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="4e742-132">INPUTS</span></span>

### <span data-ttu-id="4e742-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4e742-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4e742-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e742-134">OUTPUTS</span></span>

### <span data-ttu-id="4e742-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="4e742-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="4e742-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="4e742-136">NOTES</span></span>

<span data-ttu-id="4e742-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4e742-137">ALIASES</span></span>

<span data-ttu-id="4e742-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4e742-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e742-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4e742-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e742-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e742-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e742-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="4e742-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e742-142">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="4e742-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4e742-143">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4e742-144">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4e742-145">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4e742-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="4e742-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e742-147">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4e742-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e742-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4e742-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4e742-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="4e742-150">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4e742-151">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4e742-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4e742-152">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="4e742-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4e742-153">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="4e742-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4e742-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e742-154">RELATED LINKS</span></span>

