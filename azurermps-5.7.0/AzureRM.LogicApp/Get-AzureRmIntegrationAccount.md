---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: ee96c446ee0517363535b09ee320e04db7aeba38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519447"
---
# <span data-ttu-id="c1865-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1865-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="c1865-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1865-102">SYNOPSIS</span></span>
<span data-ttu-id="c1865-103">Ottiene gli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c1865-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1865-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1865-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1865-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1865-105">DESCRIPTION</span></span>
<span data-ttu-id="c1865-106">Il cmdlet **Get-AzureRmIntegrationAccount** ottiene gli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1865-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="c1865-107">Specificare il nome di un account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1865-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="c1865-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="c1865-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c1865-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="c1865-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c1865-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="c1865-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c1865-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="c1865-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c1865-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1865-112">EXAMPLES</span></span>

### <span data-ttu-id="c1865-113">Esempio 1: ottenere un account di integrazione per nome</span><span class="sxs-lookup"><span data-stu-id="c1865-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="c1865-114">Questo comando ottiene un account di integrazione denominato IntegrationAccount31 dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="c1865-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="c1865-115">Esempio 2: ottenere gli account di integrazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c1865-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="c1865-116">Questo comando ottiene gli account di integrazione da un gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c1865-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="c1865-117">Esempio 3: ottenere tutti gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="c1865-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="c1865-118">Questo comando consente di ottenere tutti gli account di integrazione nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c1865-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="c1865-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1865-119">PARAMETERS</span></span>

### <span data-ttu-id="c1865-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1865-120">-DefaultProfile</span></span>
<span data-ttu-id="c1865-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c1865-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1865-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1865-122">-Name</span></span>
<span data-ttu-id="c1865-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c1865-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1865-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1865-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1865-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1865-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1865-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1865-126">CommonParameters</span></span>
<span data-ttu-id="c1865-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1865-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1865-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1865-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1865-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1865-129">INPUTS</span></span>

### <span data-ttu-id="c1865-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c1865-130">None</span></span>
<span data-ttu-id="c1865-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c1865-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1865-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1865-132">OUTPUTS</span></span>

### <span data-ttu-id="c1865-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1865-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="c1865-134">Note</span><span class="sxs-lookup"><span data-stu-id="c1865-134">NOTES</span></span>

## <span data-ttu-id="c1865-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1865-135">RELATED LINKS</span></span>

[<span data-ttu-id="c1865-136">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c1865-136">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="c1865-137">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1865-137">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="c1865-138">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1865-138">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="c1865-139">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1865-139">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


