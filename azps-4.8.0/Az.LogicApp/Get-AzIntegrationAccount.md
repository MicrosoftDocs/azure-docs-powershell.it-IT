---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192457"
---
# <span data-ttu-id="efc79-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="efc79-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="efc79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efc79-102">SYNOPSIS</span></span>
<span data-ttu-id="efc79-103">Ottiene gli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="efc79-103">Gets integration accounts.</span></span>

## <span data-ttu-id="efc79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efc79-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efc79-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efc79-105">DESCRIPTION</span></span>
<span data-ttu-id="efc79-106">Il cmdlet **Get-AzIntegrationAccount** ottiene gli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc79-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="efc79-107">Specificare il nome di un account di integrazione e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc79-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="efc79-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="efc79-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="efc79-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="efc79-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="efc79-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="efc79-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="efc79-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="efc79-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="efc79-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efc79-112">EXAMPLES</span></span>

### <span data-ttu-id="efc79-113">Esempio 1: ottenere un account di integrazione per nome</span><span class="sxs-lookup"><span data-stu-id="efc79-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="efc79-114">Questo comando ottiene un account di integrazione denominato IntegrationAccount31 dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="efc79-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="efc79-115">Esempio 2: ottenere gli account di integrazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="efc79-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="efc79-116">Questo comando ottiene gli account di integrazione da un gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="efc79-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="efc79-117">Esempio 3: ottenere tutti gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="efc79-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="efc79-118">Questo comando consente di ottenere tutti gli account di integrazione nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="efc79-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="efc79-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efc79-119">PARAMETERS</span></span>

### <span data-ttu-id="efc79-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc79-120">-DefaultProfile</span></span>
<span data-ttu-id="efc79-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="efc79-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efc79-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="efc79-122">-Name</span></span>
<span data-ttu-id="efc79-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="efc79-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="efc79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc79-124">-ResourceGroupName</span></span>
<span data-ttu-id="efc79-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc79-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="efc79-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc79-126">CommonParameters</span></span>
<span data-ttu-id="efc79-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc79-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc79-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc79-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc79-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efc79-129">INPUTS</span></span>

### <span data-ttu-id="efc79-130">System. String</span><span class="sxs-lookup"><span data-stu-id="efc79-130">System.String</span></span>

## <span data-ttu-id="efc79-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efc79-131">OUTPUTS</span></span>

### <span data-ttu-id="efc79-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="efc79-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="efc79-133">Note</span><span class="sxs-lookup"><span data-stu-id="efc79-133">NOTES</span></span>

## <span data-ttu-id="efc79-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efc79-134">RELATED LINKS</span></span>

[<span data-ttu-id="efc79-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="efc79-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="efc79-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="efc79-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="efc79-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="efc79-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="efc79-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="efc79-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


