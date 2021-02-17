---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192319"
---
# <span data-ttu-id="c48c6-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c48c6-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="c48c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c48c6-103">Recupera gli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c48c6-103">Gets integration accounts.</span></span>

## <span data-ttu-id="c48c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c48c6-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c48c6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c48c6-105">DESCRIPTION</span></span>
<span data-ttu-id="c48c6-106">Il cmdlet **Get-AzIntegrationAccount** ottiene gli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c48c6-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="c48c6-107">Specificare il nome di un account di integrazione e di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c48c6-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="c48c6-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="c48c6-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c48c6-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="c48c6-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c48c6-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="c48c6-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c48c6-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="c48c6-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c48c6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c48c6-112">EXAMPLES</span></span>

### <span data-ttu-id="c48c6-113">Esempio 1: Ottenere un account di integrazione in base al nome</span><span class="sxs-lookup"><span data-stu-id="c48c6-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c48c6-114">Questo comando recupera un account di integrazione denominato IntegrationAccount31 dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="c48c6-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="c48c6-115">Esempio 2: Ottenere account di integrazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c48c6-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c48c6-116">Questo comando recupera gli account di integrazione da un gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c48c6-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c48c6-117">Esempio 3: Ottenere tutti gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="c48c6-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="c48c6-118">Questo comando recupera tutti gli account di integrazione nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c48c6-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="c48c6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c48c6-119">PARAMETERS</span></span>

### <span data-ttu-id="c48c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48c6-120">-DefaultProfile</span></span>
<span data-ttu-id="c48c6-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="c48c6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48c6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c48c6-122">-Name</span></span>
<span data-ttu-id="c48c6-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c48c6-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="c48c6-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c48c6-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48c6-126">CommonParameters</span></span>
<span data-ttu-id="c48c6-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48c6-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48c6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48c6-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c48c6-129">INPUTS</span></span>

### <span data-ttu-id="c48c6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c48c6-130">System.String</span></span>

## <span data-ttu-id="c48c6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c48c6-131">OUTPUTS</span></span>

### <span data-ttu-id="c48c6-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c48c6-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="c48c6-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c48c6-133">NOTES</span></span>

## <span data-ttu-id="c48c6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c48c6-134">RELATED LINKS</span></span>

[<span data-ttu-id="c48c6-135">Get-AzIntegrationAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c48c6-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="c48c6-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c48c6-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="c48c6-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c48c6-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="c48c6-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c48c6-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


