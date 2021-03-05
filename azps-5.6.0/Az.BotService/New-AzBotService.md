---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 11f3124c98e84dcaec40c3b8ecd9b8831b572617
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009294"
---
# <span data-ttu-id="3fc34-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="3fc34-101">New-AzBotService</span></span>

## <span data-ttu-id="3fc34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fc34-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc34-103">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="3fc34-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3fc34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fc34-104">SYNTAX</span></span>

### <span data-ttu-id="3fc34-105">Registrazione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fc34-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3fc34-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="3fc34-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3fc34-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3fc34-107">DESCRIPTION</span></span>
<span data-ttu-id="3fc34-108">Restituisce un servizio BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="3fc34-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3fc34-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fc34-109">EXAMPLES</span></span>

### <span data-ttu-id="3fc34-110">Esempio 1: Creare un nuovo bot</span><span class="sxs-lookup"><span data-stu-id="3fc34-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="3fc34-111">Creare un nuovo bot in base a ResourceGroupName e ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3fc34-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="3fc34-112">Esempio 2: Creare una nuova app Web</span><span class="sxs-lookup"><span data-stu-id="3fc34-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="3fc34-113">Creare una nuova app Web in base a ResourceGroupName e ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3fc34-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="3fc34-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fc34-114">PARAMETERS</span></span>

### <span data-ttu-id="3fc34-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3fc34-115">-ApplicationId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="3fc34-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="3fc34-117">-BotTemplateType</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc34-118">-DefaultProfile</span></span>
<span data-ttu-id="3fc34-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fc34-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fc34-120">-Description</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3fc34-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-122">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="3fc34-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="3fc34-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-124">-Lingua</span><span class="sxs-lookup"><span data-stu-id="3fc34-124">-Language</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-125">-Location</span><span class="sxs-lookup"><span data-stu-id="3fc34-125">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3fc34-126">-Name</span></span>
<span data-ttu-id="3fc34-127">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="3fc34-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-128">-Registration</span><span class="sxs-lookup"><span data-stu-id="3fc34-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc34-129">-ResourceGroupName</span></span>
<span data-ttu-id="3fc34-130">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3fc34-130">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="3fc34-131">-Sku</span></span>
<span data-ttu-id="3fc34-132">Nome della SKU</span><span class="sxs-lookup"><span data-stu-id="3fc34-132">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fc34-133">-SubscriptionId</span></span>
<span data-ttu-id="3fc34-134">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc34-134">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="3fc34-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc34-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc34-136">CommonParameters</span></span>
<span data-ttu-id="3fc34-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc34-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc34-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3fc34-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc34-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="3fc34-139">INPUTS</span></span>

## <span data-ttu-id="3fc34-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fc34-140">OUTPUTS</span></span>

### <span data-ttu-id="3fc34-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="3fc34-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="3fc34-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="3fc34-142">NOTES</span></span>

<span data-ttu-id="3fc34-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3fc34-143">ALIASES</span></span>

## <span data-ttu-id="3fc34-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fc34-144">RELATED LINKS</span></span>

