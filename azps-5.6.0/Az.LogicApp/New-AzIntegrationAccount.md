---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: 12fb8ed21365c3fd0decf3272364e30c8b8dc6cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008862"
---
# <span data-ttu-id="fe322-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fe322-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="fe322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe322-102">SYNOPSIS</span></span>
<span data-ttu-id="fe322-103">Crea un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe322-103">Creates an integration account.</span></span>

## <span data-ttu-id="fe322-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe322-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe322-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fe322-105">DESCRIPTION</span></span>
<span data-ttu-id="fe322-106">Il cmdlet **New-AzIntegrationAccount** crea un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe322-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="fe322-107">Questo cmdlet restituisce un oggetto che rappresenta l'account di integrazione. Specificare un nome, una posizione, un nome di gruppo di risorse e un nome SKU.</span><span class="sxs-lookup"><span data-stu-id="fe322-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="fe322-108">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="fe322-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="fe322-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="fe322-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fe322-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="fe322-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fe322-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="fe322-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fe322-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="fe322-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fe322-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe322-113">EXAMPLES</span></span>

### <span data-ttu-id="fe322-114">Esempio 1: Creare un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="fe322-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="fe322-115">Questo comando crea un account di integrazione denominato IntegrationAccount31 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="fe322-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="fe322-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe322-116">PARAMETERS</span></span>

### <span data-ttu-id="fe322-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe322-117">-DefaultProfile</span></span>
<span data-ttu-id="fe322-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="fe322-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe322-119">-Location</span><span class="sxs-lookup"><span data-stu-id="fe322-119">-Location</span></span>
<span data-ttu-id="fe322-120">Specifica una posizione per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe322-120">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe322-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fe322-121">-Name</span></span>
<span data-ttu-id="fe322-122">Specifica un nome per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe322-122">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe322-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe322-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe322-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe322-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe322-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe322-125">-Sku</span></span>
<span data-ttu-id="fe322-126">Specifica un nome di SKU per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fe322-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe322-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe322-127">-Confirm</span></span>
<span data-ttu-id="fe322-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe322-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe322-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe322-129">-WhatIf</span></span>
<span data-ttu-id="fe322-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe322-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe322-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe322-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe322-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe322-132">CommonParameters</span></span>
<span data-ttu-id="fe322-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe322-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe322-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe322-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe322-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="fe322-135">INPUTS</span></span>

### <span data-ttu-id="fe322-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fe322-136">System.String</span></span>

## <span data-ttu-id="fe322-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe322-137">OUTPUTS</span></span>

### <span data-ttu-id="fe322-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fe322-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="fe322-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="fe322-139">NOTES</span></span>

## <span data-ttu-id="fe322-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe322-140">RELATED LINKS</span></span>

[<span data-ttu-id="fe322-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fe322-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="fe322-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fe322-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="fe322-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fe322-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


