---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: 67a49250607e1c7d70f1799aa26bd866924b5edc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475373"
---
# <span data-ttu-id="7210a-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="7210a-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="7210a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7210a-102">SYNOPSIS</span></span>
<span data-ttu-id="7210a-103">Ottenere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7210a-103">Get an application.</span></span>

## <span data-ttu-id="7210a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7210a-104">SYNTAX</span></span>

### <span data-ttu-id="7210a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7210a-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7210a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7210a-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7210a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7210a-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7210a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7210a-108">DESCRIPTION</span></span>
<span data-ttu-id="7210a-109">Ottenere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7210a-109">Get an application.</span></span>

## <span data-ttu-id="7210a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7210a-110">EXAMPLES</span></span>

### <span data-ttu-id="7210a-111">Esempio 1: ottenere un'applicazione desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="7210a-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="7210a-112">Questo comando consente di ottenere un'applicazione desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="7210a-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="7210a-113">Esempio 2: elencare le applicazioni desktop virtuali di Windows</span><span class="sxs-lookup"><span data-stu-id="7210a-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="7210a-114">Questo comando elenca le applicazioni desktop virtuali di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="7210a-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="7210a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7210a-115">PARAMETERS</span></span>

### <span data-ttu-id="7210a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7210a-116">-DefaultProfile</span></span>
<span data-ttu-id="7210a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7210a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7210a-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="7210a-118">-GroupName</span></span>
<span data-ttu-id="7210a-119">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="7210a-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7210a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7210a-120">-InputObject</span></span>
<span data-ttu-id="7210a-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7210a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7210a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7210a-122">-Name</span></span>
<span data-ttu-id="7210a-123">Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="7210a-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7210a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7210a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7210a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7210a-125">The name of the resource group.</span></span>
<span data-ttu-id="7210a-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7210a-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7210a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7210a-127">-SubscriptionId</span></span>
<span data-ttu-id="7210a-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7210a-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7210a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7210a-129">CommonParameters</span></span>
<span data-ttu-id="7210a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7210a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7210a-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7210a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7210a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7210a-132">INPUTS</span></span>

### <span data-ttu-id="7210a-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="7210a-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7210a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7210a-134">OUTPUTS</span></span>

### <span data-ttu-id="7210a-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="7210a-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="7210a-136">Note</span><span class="sxs-lookup"><span data-stu-id="7210a-136">NOTES</span></span>

<span data-ttu-id="7210a-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7210a-137">ALIASES</span></span>

<span data-ttu-id="7210a-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7210a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7210a-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7210a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7210a-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7210a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7210a-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7210a-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7210a-142">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="7210a-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7210a-143">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="7210a-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7210a-144">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="7210a-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7210a-145">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="7210a-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7210a-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="7210a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7210a-147">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="7210a-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="7210a-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7210a-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7210a-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7210a-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="7210a-150">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="7210a-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7210a-151">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7210a-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7210a-152">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="7210a-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7210a-153">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="7210a-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7210a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7210a-154">RELATED LINKS</span></span>

