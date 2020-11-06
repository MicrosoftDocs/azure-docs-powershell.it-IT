---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: d2948378f9312687e2dbbe09bd7c583cbe085778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514264"
---
# <span data-ttu-id="2e844-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2e844-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="2e844-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e844-102">SYNOPSIS</span></span>
<span data-ttu-id="2e844-103">Modifica un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2e844-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e844-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e844-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e844-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e844-105">DESCRIPTION</span></span>
<span data-ttu-id="2e844-106">Il cmdlet **set-AzureRmIntegrationAccount** modifica un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2e844-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="2e844-107">Questo cmdlet restituisce un oggetto che rappresenta l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2e844-107">This cmdlet returns an object that represents the integration account.</span></span>

<span data-ttu-id="2e844-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="2e844-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2e844-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="2e844-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2e844-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="2e844-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2e844-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="2e844-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2e844-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e844-112">EXAMPLES</span></span>

### <span data-ttu-id="2e844-113">Esempio 1: modificare un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2e844-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="2e844-114">Questo comando modifica un account di integrazione denominato IntegrationAccount31 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="2e844-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="2e844-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e844-115">PARAMETERS</span></span>

### <span data-ttu-id="2e844-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e844-116">-DefaultProfile</span></span>
<span data-ttu-id="2e844-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2e844-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e844-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2e844-118">-Force</span></span>
<span data-ttu-id="2e844-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2e844-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e844-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2e844-120">-Location</span></span>
<span data-ttu-id="2e844-121">Specifica un percorso per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2e844-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="2e844-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e844-122">-Name</span></span>
<span data-ttu-id="2e844-123">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2e844-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e844-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e844-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e844-125">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e844-125">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e844-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="2e844-126">-Sku</span></span>
<span data-ttu-id="2e844-127">Specifica un nome di SKU per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="2e844-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="2e844-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e844-128">-Confirm</span></span>
<span data-ttu-id="2e844-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e844-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e844-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e844-130">-WhatIf</span></span>
<span data-ttu-id="2e844-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e844-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e844-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e844-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e844-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e844-133">CommonParameters</span></span>
<span data-ttu-id="2e844-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e844-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e844-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e844-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e844-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e844-136">INPUTS</span></span>

### <span data-ttu-id="2e844-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2e844-137">None</span></span>
<span data-ttu-id="2e844-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2e844-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e844-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e844-139">OUTPUTS</span></span>

### <span data-ttu-id="2e844-140">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2e844-140">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="2e844-141">Note</span><span class="sxs-lookup"><span data-stu-id="2e844-141">NOTES</span></span>

## <span data-ttu-id="2e844-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e844-142">RELATED LINKS</span></span>

[<span data-ttu-id="2e844-143">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2e844-143">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="2e844-144">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2e844-144">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="2e844-145">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2e844-145">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


