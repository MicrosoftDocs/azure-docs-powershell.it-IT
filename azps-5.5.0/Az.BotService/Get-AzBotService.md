---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181903"
---
# <span data-ttu-id="362fa-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="362fa-101">Get-AzBotService</span></span>

## <span data-ttu-id="362fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="362fa-102">SYNOPSIS</span></span>
<span data-ttu-id="362fa-103">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="362fa-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="362fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="362fa-104">SYNTAX</span></span>

### <span data-ttu-id="362fa-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="362fa-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="362fa-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="362fa-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="362fa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="362fa-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="362fa-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="362fa-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="362fa-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="362fa-109">DESCRIPTION</span></span>
<span data-ttu-id="362fa-110">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="362fa-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="362fa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="362fa-111">EXAMPLES</span></span>

### <span data-ttu-id="362fa-112">Esempio 1: Ottenere tutti i BotServices</span><span class="sxs-lookup"><span data-stu-id="362fa-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="362fa-113">Ottieni tutti i BotServices</span><span class="sxs-lookup"><span data-stu-id="362fa-113">Get all BotServices</span></span>

### <span data-ttu-id="362fa-114">Esempio 2: Ottenere BotService dal nome e dal nome ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362fa-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="362fa-115">Ottenere BotService per ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="362fa-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="362fa-116">Esempio 3: Ottenere tutti i BotServices per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362fa-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="362fa-117">Ottenere tutti i BotServices per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362fa-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="362fa-118">Esempio 4: Ottenere BotService da inputObject</span><span class="sxs-lookup"><span data-stu-id="362fa-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="362fa-119">Ottenere BotService da inputObject</span><span class="sxs-lookup"><span data-stu-id="362fa-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="362fa-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="362fa-120">PARAMETERS</span></span>

### <span data-ttu-id="362fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362fa-121">-DefaultProfile</span></span>
<span data-ttu-id="362fa-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="362fa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="362fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="362fa-123">-InputObject</span></span>
<span data-ttu-id="362fa-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="362fa-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="362fa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="362fa-125">-Name</span></span>
<span data-ttu-id="362fa-126">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="362fa-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362fa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362fa-127">-ResourceGroupName</span></span>
<span data-ttu-id="362fa-128">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="362fa-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="362fa-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="362fa-129">-SubscriptionId</span></span>
<span data-ttu-id="362fa-130">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="362fa-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="362fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362fa-131">CommonParameters</span></span>
<span data-ttu-id="362fa-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362fa-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="362fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362fa-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="362fa-134">INPUTS</span></span>

### <span data-ttu-id="362fa-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="362fa-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="362fa-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="362fa-136">OUTPUTS</span></span>

### <span data-ttu-id="362fa-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="362fa-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="362fa-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="362fa-138">NOTES</span></span>

<span data-ttu-id="362fa-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="362fa-139">ALIASES</span></span>

<span data-ttu-id="362fa-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="362fa-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="362fa-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="362fa-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="362fa-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="362fa-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="362fa-143">INPUTOBJECT <IBotServiceIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="362fa-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="362fa-144">`[ChannelName <ChannelName?>]`: nome della risorsa Canale.</span><span class="sxs-lookup"><span data-stu-id="362fa-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="362fa-145">`[ConnectionName <String>]`: nome della risorsa impostazione di connessione al servizio Bot</span><span class="sxs-lookup"><span data-stu-id="362fa-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="362fa-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="362fa-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="362fa-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="362fa-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="362fa-148">`[ResourceName <String>]`: nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="362fa-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="362fa-149">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="362fa-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="362fa-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="362fa-150">RELATED LINKS</span></span>

