---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: ec1e223359c3d83a3cfb77810e0e680f7142bc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520065"
---
# <span data-ttu-id="53220-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="53220-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="53220-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53220-102">SYNOPSIS</span></span>
<span data-ttu-id="53220-103">Crea un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="53220-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53220-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53220-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53220-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53220-105">DESCRIPTION</span></span>
<span data-ttu-id="53220-106">Il cmdlet **New-AzureRmIntegrationAccount** crea un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="53220-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="53220-107">Questo cmdlet restituisce un oggetto che rappresenta l'account di integrazione. Specificare un nome, un percorso, un nome del gruppo di risorse e un nome SKU.</span><span class="sxs-lookup"><span data-stu-id="53220-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="53220-108">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="53220-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="53220-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="53220-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="53220-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="53220-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="53220-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="53220-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="53220-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="53220-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="53220-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53220-113">EXAMPLES</span></span>

### <span data-ttu-id="53220-114">Esempio 1: creare un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="53220-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="53220-115">Questo comando crea un account di integrazione denominato IntegrationAccount31 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="53220-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="53220-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53220-116">PARAMETERS</span></span>

### <span data-ttu-id="53220-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="53220-117">-Location</span></span>
<span data-ttu-id="53220-118">Specifica un percorso per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="53220-118">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="53220-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="53220-119">-Name</span></span>
<span data-ttu-id="53220-120">Specifica un nome per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="53220-120">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="53220-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53220-121">-ResourceGroupName</span></span>
<span data-ttu-id="53220-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="53220-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="53220-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="53220-123">-Sku</span></span>
<span data-ttu-id="53220-124">Specifica un nome di SKU per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="53220-124">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="53220-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53220-125">-Confirm</span></span>
<span data-ttu-id="53220-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53220-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53220-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53220-127">-WhatIf</span></span>
<span data-ttu-id="53220-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53220-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53220-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53220-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53220-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53220-130">-DefaultProfile</span></span>
<span data-ttu-id="53220-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53220-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53220-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53220-132">CommonParameters</span></span>
<span data-ttu-id="53220-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53220-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53220-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53220-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53220-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53220-135">INPUTS</span></span>

## <span data-ttu-id="53220-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53220-136">OUTPUTS</span></span>

### <span data-ttu-id="53220-137">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="53220-137">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="53220-138">Note</span><span class="sxs-lookup"><span data-stu-id="53220-138">NOTES</span></span>

## <span data-ttu-id="53220-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53220-139">RELATED LINKS</span></span>

[<span data-ttu-id="53220-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="53220-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="53220-141">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="53220-141">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="53220-142">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="53220-142">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


