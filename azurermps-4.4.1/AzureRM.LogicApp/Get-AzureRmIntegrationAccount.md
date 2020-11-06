---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: 441681cd33fe7715fbbb6fb244848c287f14ebb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510560"
---
# <span data-ttu-id="21d3b-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="21d3b-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="21d3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="21d3b-103">Ottiene gli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="21d3b-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21d3b-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21d3b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="21d3b-106">Il cmdlet **Get-AzureRmIntegrationAccount** ottiene gli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21d3b-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="21d3b-107">Specificare il nome di un account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21d3b-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="21d3b-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="21d3b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="21d3b-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="21d3b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="21d3b-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="21d3b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="21d3b-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="21d3b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="21d3b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21d3b-112">EXAMPLES</span></span>

### <span data-ttu-id="21d3b-113">Esempio 1: ottenere un account di integrazione per nome</span><span class="sxs-lookup"><span data-stu-id="21d3b-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="21d3b-114">Questo comando ottiene un account di integrazione denominato IntegrationAccount31 dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="21d3b-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="21d3b-115">Esempio 2: ottenere gli account di integrazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="21d3b-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="21d3b-116">Questo comando ottiene gli account di integrazione da un gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="21d3b-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="21d3b-117">Esempio 3: ottenere tutti gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="21d3b-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="21d3b-118">Questo comando consente di ottenere tutti gli account di integrazione nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="21d3b-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="21d3b-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21d3b-119">PARAMETERS</span></span>

### <span data-ttu-id="21d3b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="21d3b-120">-Name</span></span>
<span data-ttu-id="21d3b-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="21d3b-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="21d3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="21d3b-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21d3b-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="21d3b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d3b-124">-DefaultProfile</span></span>
<span data-ttu-id="21d3b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21d3b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d3b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d3b-126">CommonParameters</span></span>
<span data-ttu-id="21d3b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d3b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d3b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d3b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d3b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21d3b-129">INPUTS</span></span>

## <span data-ttu-id="21d3b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21d3b-130">OUTPUTS</span></span>

### <span data-ttu-id="21d3b-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="21d3b-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="21d3b-132">Note</span><span class="sxs-lookup"><span data-stu-id="21d3b-132">NOTES</span></span>

## <span data-ttu-id="21d3b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21d3b-133">RELATED LINKS</span></span>

[<span data-ttu-id="21d3b-134">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="21d3b-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="21d3b-135">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="21d3b-135">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="21d3b-136">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="21d3b-136">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="21d3b-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="21d3b-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


