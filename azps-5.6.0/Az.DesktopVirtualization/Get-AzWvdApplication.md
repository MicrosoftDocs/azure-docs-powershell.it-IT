---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: b7aa21b07726140f8f6514fe8d7b6dc9a4b191dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962061"
---
# <span data-ttu-id="459ac-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="459ac-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="459ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="459ac-102">SYNOPSIS</span></span>
<span data-ttu-id="459ac-103">Ottenere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="459ac-103">Get an application.</span></span>

## <span data-ttu-id="459ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="459ac-104">SYNTAX</span></span>

### <span data-ttu-id="459ac-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="459ac-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="459ac-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="459ac-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="459ac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="459ac-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="459ac-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="459ac-108">DESCRIPTION</span></span>
<span data-ttu-id="459ac-109">Ottenere un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="459ac-109">Get an application.</span></span>

## <span data-ttu-id="459ac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="459ac-110">EXAMPLES</span></span>

### <span data-ttu-id="459ac-111">Esempio 1: Ottenere un'applicazione Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="459ac-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="459ac-112">Questo comando recupera un'applicazione Desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="459ac-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="459ac-113">Esempio 2: Elencare le applicazioni Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="459ac-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="459ac-114">Questo comando elenca le applicazioni Desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="459ac-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="459ac-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="459ac-115">PARAMETERS</span></span>

### <span data-ttu-id="459ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459ac-116">-DefaultProfile</span></span>
<span data-ttu-id="459ac-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="459ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="459ac-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="459ac-118">-GroupName</span></span>
<span data-ttu-id="459ac-119">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="459ac-119">The name of the application group</span></span>

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

### <span data-ttu-id="459ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="459ac-120">-InputObject</span></span>
<span data-ttu-id="459ac-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="459ac-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="459ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="459ac-122">-Name</span></span>
<span data-ttu-id="459ac-123">Nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="459ac-123">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="459ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="459ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="459ac-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="459ac-125">The name of the resource group.</span></span>
<span data-ttu-id="459ac-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="459ac-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="459ac-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="459ac-127">-SubscriptionId</span></span>
<span data-ttu-id="459ac-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="459ac-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="459ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459ac-129">CommonParameters</span></span>
<span data-ttu-id="459ac-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="459ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459ac-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="459ac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459ac-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="459ac-132">INPUTS</span></span>

### <span data-ttu-id="459ac-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="459ac-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="459ac-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="459ac-134">OUTPUTS</span></span>

### <span data-ttu-id="459ac-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="459ac-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="459ac-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="459ac-136">NOTES</span></span>

<span data-ttu-id="459ac-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="459ac-137">ALIASES</span></span>

<span data-ttu-id="459ac-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="459ac-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="459ac-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="459ac-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="459ac-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="459ac-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="459ac-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="459ac-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="459ac-142">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="459ac-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="459ac-143">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="459ac-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="459ac-144">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="459ac-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="459ac-145">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="459ac-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="459ac-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="459ac-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="459ac-147">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="459ac-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="459ac-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="459ac-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="459ac-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="459ac-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="459ac-150">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="459ac-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="459ac-151">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="459ac-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="459ac-152">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="459ac-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="459ac-153">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="459ac-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="459ac-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="459ac-154">RELATED LINKS</span></span>

