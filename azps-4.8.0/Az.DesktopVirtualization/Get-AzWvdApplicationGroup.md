---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031783"
---
# <span data-ttu-id="89770-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="89770-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="89770-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89770-102">SYNOPSIS</span></span>
<span data-ttu-id="89770-103">Ottenere un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="89770-103">Get an application group.</span></span>

## <span data-ttu-id="89770-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89770-104">SYNTAX</span></span>

### <span data-ttu-id="89770-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89770-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="89770-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="89770-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="89770-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89770-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="89770-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="89770-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="89770-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89770-109">DESCRIPTION</span></span>
<span data-ttu-id="89770-110">Ottenere un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="89770-110">Get an application group.</span></span>

## <span data-ttu-id="89770-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89770-111">EXAMPLES</span></span>

### <span data-ttu-id="89770-112">Esempio 1: ottenere un desktop virtuale di Windows ApplicationGroup per nome</span><span class="sxs-lookup"><span data-stu-id="89770-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="89770-113">Questo comando consente di ottenere un ApplicationGroup desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89770-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="89770-114">Esempio 2: elenco di Windows Virtual Desktop ApplicationGroups</span><span class="sxs-lookup"><span data-stu-id="89770-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="89770-115">Questo comando elenca un ApplicationGroups desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89770-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="89770-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89770-116">PARAMETERS</span></span>

### <span data-ttu-id="89770-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89770-117">-DefaultProfile</span></span>
<span data-ttu-id="89770-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89770-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89770-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="89770-119">-Filter</span></span>
<span data-ttu-id="89770-120">Espressione di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="89770-120">OData filter expression.</span></span>
<span data-ttu-id="89770-121">Le proprietà valide per il filtro sono applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="89770-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="89770-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89770-122">-InputObject</span></span>
<span data-ttu-id="89770-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="89770-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="89770-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="89770-124">-Name</span></span>
<span data-ttu-id="89770-125">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="89770-125">The name of the application group</span></span>

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

### <span data-ttu-id="89770-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89770-126">-ResourceGroupName</span></span>
<span data-ttu-id="89770-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89770-127">The name of the resource group.</span></span>
<span data-ttu-id="89770-128">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="89770-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="89770-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89770-129">-SubscriptionId</span></span>
<span data-ttu-id="89770-130">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89770-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="89770-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89770-131">CommonParameters</span></span>
<span data-ttu-id="89770-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89770-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89770-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89770-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89770-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89770-134">INPUTS</span></span>

### <span data-ttu-id="89770-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="89770-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="89770-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89770-136">OUTPUTS</span></span>

### <span data-ttu-id="89770-137">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="89770-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="89770-138">Note</span><span class="sxs-lookup"><span data-stu-id="89770-138">NOTES</span></span>

<span data-ttu-id="89770-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="89770-139">ALIASES</span></span>

<span data-ttu-id="89770-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89770-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89770-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="89770-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89770-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89770-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89770-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="89770-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89770-144">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="89770-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="89770-145">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="89770-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="89770-146">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="89770-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="89770-147">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="89770-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="89770-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="89770-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89770-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89770-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="89770-150">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="89770-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="89770-151">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="89770-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="89770-152">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="89770-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="89770-153">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="89770-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="89770-154">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="89770-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="89770-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89770-155">RELATED LINKS</span></span>

