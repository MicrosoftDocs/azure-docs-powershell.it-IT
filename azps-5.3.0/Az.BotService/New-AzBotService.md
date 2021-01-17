---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478048"
---
# <span data-ttu-id="565b6-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="565b6-101">New-AzBotService</span></span>

## <span data-ttu-id="565b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="565b6-102">SYNOPSIS</span></span>
<span data-ttu-id="565b6-103">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="565b6-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="565b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="565b6-104">SYNTAX</span></span>

### <span data-ttu-id="565b6-105">Registrazione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="565b6-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="565b6-106">Web App</span><span class="sxs-lookup"><span data-stu-id="565b6-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="565b6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="565b6-107">DESCRIPTION</span></span>
<span data-ttu-id="565b6-108">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="565b6-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="565b6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="565b6-109">EXAMPLES</span></span>

### <span data-ttu-id="565b6-110">Esempio 1: creare un nuovo bot</span><span class="sxs-lookup"><span data-stu-id="565b6-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="565b6-111">Creare un nuovo bot da ResourceGroupName e ApplicationId</span><span class="sxs-lookup"><span data-stu-id="565b6-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="565b6-112">Esempio 2: creare una nuova app Web</span><span class="sxs-lookup"><span data-stu-id="565b6-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="565b6-113">Creare una nuova app Web per ResourceGroupName e ApplicationId</span><span class="sxs-lookup"><span data-stu-id="565b6-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="565b6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="565b6-114">PARAMETERS</span></span>

### <span data-ttu-id="565b6-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="565b6-115">-ApplicationId</span></span>


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

### <span data-ttu-id="565b6-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="565b6-116">-ApplicationSecret</span></span>


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

### <span data-ttu-id="565b6-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="565b6-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="565b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565b6-118">-DefaultProfile</span></span>
<span data-ttu-id="565b6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="565b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="565b6-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="565b6-120">-Description</span></span>


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

### <span data-ttu-id="565b6-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="565b6-121">-DisplayName</span></span>


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

### <span data-ttu-id="565b6-122">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="565b6-122">-Endpoint</span></span>


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

### <span data-ttu-id="565b6-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="565b6-123">-ExistingServerFarmId</span></span>


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

### <span data-ttu-id="565b6-124">-Lingua</span><span class="sxs-lookup"><span data-stu-id="565b6-124">-Language</span></span>


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

### <span data-ttu-id="565b6-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="565b6-125">-Location</span></span>


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

### <span data-ttu-id="565b6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="565b6-126">-Name</span></span>
<span data-ttu-id="565b6-127">Il nome della risorsa bot.</span><span class="sxs-lookup"><span data-stu-id="565b6-127">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="565b6-128">-Registrazione</span><span class="sxs-lookup"><span data-stu-id="565b6-128">-Registration</span></span>


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

### <span data-ttu-id="565b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="565b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="565b6-130">Nome del gruppo di risorse bot nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="565b6-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="565b6-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="565b6-131">-Sku</span></span>
<span data-ttu-id="565b6-132">Nome Usk</span><span class="sxs-lookup"><span data-stu-id="565b6-132">The sku name</span></span>

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

### <span data-ttu-id="565b6-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="565b6-133">-SubscriptionId</span></span>
<span data-ttu-id="565b6-134">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="565b6-134">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="565b6-135">-Web App</span><span class="sxs-lookup"><span data-stu-id="565b6-135">-Webapp</span></span>


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

### <span data-ttu-id="565b6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565b6-136">CommonParameters</span></span>
<span data-ttu-id="565b6-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565b6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565b6-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="565b6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565b6-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="565b6-139">INPUTS</span></span>

## <span data-ttu-id="565b6-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="565b6-140">OUTPUTS</span></span>

### <span data-ttu-id="565b6-141">Microsoft. Azure. PowerShell. Cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="565b6-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="565b6-142">Note</span><span class="sxs-lookup"><span data-stu-id="565b6-142">NOTES</span></span>

<span data-ttu-id="565b6-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="565b6-143">ALIASES</span></span>

## <span data-ttu-id="565b6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="565b6-144">RELATED LINKS</span></span>

