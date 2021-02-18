---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 480c1d5517aa79ff7b3a0fa5dfa24f2ae6f4ae45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200518"
---
# <span data-ttu-id="39149-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="39149-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="39149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39149-102">SYNOPSIS</span></span>
<span data-ttu-id="39149-103">Ottenere un pool host.</span><span class="sxs-lookup"><span data-stu-id="39149-103">Get a host pool.</span></span>

## <span data-ttu-id="39149-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39149-104">SYNTAX</span></span>

### <span data-ttu-id="39149-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39149-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39149-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="39149-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39149-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39149-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="39149-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="39149-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="39149-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39149-109">DESCRIPTION</span></span>
<span data-ttu-id="39149-110">Ottenere un pool host.</span><span class="sxs-lookup"><span data-stu-id="39149-110">Get a host pool.</span></span>

## <span data-ttu-id="39149-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39149-111">EXAMPLES</span></span>

### <span data-ttu-id="39149-112">Esempio 1: Ottenere un pool Host Desktop virtuale Di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="39149-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="39149-113">Questo comando ottiene un pool di desktop virtuali Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39149-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="39149-114">Esempio 2: Elencare i pool di desktop virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="39149-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="39149-115">Questo comando elenca i pool di desktop virtuali Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39149-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="39149-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39149-116">PARAMETERS</span></span>

### <span data-ttu-id="39149-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39149-117">-DefaultProfile</span></span>
<span data-ttu-id="39149-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39149-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39149-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39149-119">-InputObject</span></span>
<span data-ttu-id="39149-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="39149-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39149-121">-Name</span><span class="sxs-lookup"><span data-stu-id="39149-121">-Name</span></span>
<span data-ttu-id="39149-122">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="39149-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39149-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39149-123">-ResourceGroupName</span></span>
<span data-ttu-id="39149-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39149-124">The name of the resource group.</span></span>
<span data-ttu-id="39149-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="39149-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="39149-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39149-126">-SubscriptionId</span></span>
<span data-ttu-id="39149-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39149-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="39149-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39149-128">CommonParameters</span></span>
<span data-ttu-id="39149-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39149-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39149-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39149-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39149-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="39149-131">INPUTS</span></span>

### <span data-ttu-id="39149-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="39149-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="39149-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39149-133">OUTPUTS</span></span>

### <span data-ttu-id="39149-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="39149-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="39149-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="39149-135">NOTES</span></span>

<span data-ttu-id="39149-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="39149-136">ALIASES</span></span>

<span data-ttu-id="39149-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="39149-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39149-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="39149-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39149-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39149-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39149-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="39149-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39149-141">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="39149-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="39149-142">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="39149-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="39149-143">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="39149-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="39149-144">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="39149-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="39149-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="39149-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39149-146">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="39149-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="39149-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39149-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="39149-148">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="39149-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="39149-149">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="39149-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="39149-150">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39149-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="39149-151">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="39149-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="39149-152">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="39149-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="39149-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39149-153">RELATED LINKS</span></span>

