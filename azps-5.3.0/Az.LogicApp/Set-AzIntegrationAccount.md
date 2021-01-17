---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476136"
---
# <span data-ttu-id="fcf2a-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fcf2a-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="fcf2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcf2a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf2a-103">Modifica un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-103">Modifies an integration account.</span></span>

## <span data-ttu-id="fcf2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcf2a-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcf2a-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf2a-106">Il cmdlet **set-AzIntegrationAccount** modifica un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="fcf2a-107">Questo cmdlet restituisce un oggetto che rappresenta l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="fcf2a-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fcf2a-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fcf2a-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fcf2a-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fcf2a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcf2a-112">EXAMPLES</span></span>

### <span data-ttu-id="fcf2a-113">Esempio 1: modificare un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="fcf2a-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="fcf2a-114">Questo comando modifica un account di integrazione denominato IntegrationAccount31 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="fcf2a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcf2a-115">PARAMETERS</span></span>

### <span data-ttu-id="fcf2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf2a-116">-DefaultProfile</span></span>
<span data-ttu-id="fcf2a-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fcf2a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcf2a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fcf2a-118">-Force</span></span>
<span data-ttu-id="fcf2a-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf2a-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fcf2a-120">-Location</span></span>
<span data-ttu-id="fcf2a-121">Specifica un percorso per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="fcf2a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcf2a-122">-Name</span></span>
<span data-ttu-id="fcf2a-123">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="fcf2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="fcf2a-125">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fcf2a-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="fcf2a-126">-Sku</span></span>
<span data-ttu-id="fcf2a-127">Specifica un nome di SKU per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="fcf2a-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fcf2a-128">-Confirm</span></span>
<span data-ttu-id="fcf2a-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf2a-130">-WhatIf</span></span>
<span data-ttu-id="fcf2a-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf2a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf2a-133">CommonParameters</span></span>
<span data-ttu-id="fcf2a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf2a-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf2a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf2a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcf2a-136">INPUTS</span></span>

### <span data-ttu-id="fcf2a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fcf2a-137">System.String</span></span>

## <span data-ttu-id="fcf2a-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcf2a-138">OUTPUTS</span></span>

### <span data-ttu-id="fcf2a-139">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fcf2a-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="fcf2a-140">Note</span><span class="sxs-lookup"><span data-stu-id="fcf2a-140">NOTES</span></span>

## <span data-ttu-id="fcf2a-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcf2a-141">RELATED LINKS</span></span>

[<span data-ttu-id="fcf2a-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fcf2a-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="fcf2a-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fcf2a-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="fcf2a-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fcf2a-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


