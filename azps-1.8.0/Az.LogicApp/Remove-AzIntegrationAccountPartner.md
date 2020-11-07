---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: d630a88134b2910a38b21ff964db9748db5cbeeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835416"
---
# <span data-ttu-id="cdf5c-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdf5c-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="cdf5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdf5c-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf5c-103">Rimuove un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="cdf5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdf5c-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdf5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdf5c-105">DESCRIPTION</span></span>
<span data-ttu-id="cdf5c-106">Il cmdlet **Remove-AzIntegrationAccountPartner** rimuove un partner dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="cdf5c-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="cdf5c-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cdf5c-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cdf5c-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cdf5c-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cdf5c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdf5c-112">EXAMPLES</span></span>

### <span data-ttu-id="cdf5c-113">Esempio 1: rimuovere un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="cdf5c-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="cdf5c-114">Questo comando rimuove il partner account di integrazione denominato IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="cdf5c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdf5c-115">PARAMETERS</span></span>

### <span data-ttu-id="cdf5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf5c-116">-DefaultProfile</span></span>
<span data-ttu-id="cdf5c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cdf5c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdf5c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cdf5c-118">-Force</span></span>
<span data-ttu-id="cdf5c-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdf5c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdf5c-120">-Name</span></span>
<span data-ttu-id="cdf5c-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf5c-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="cdf5c-122">-PartnerName</span></span>
<span data-ttu-id="cdf5c-123">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="cdf5c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdf5c-124">-ResourceGroupName</span></span>
<span data-ttu-id="cdf5c-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cdf5c-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdf5c-126">-Confirm</span></span>
<span data-ttu-id="cdf5c-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdf5c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdf5c-128">-WhatIf</span></span>
<span data-ttu-id="cdf5c-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdf5c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdf5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf5c-131">CommonParameters</span></span>
<span data-ttu-id="cdf5c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf5c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdf5c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf5c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdf5c-134">INPUTS</span></span>

### <span data-ttu-id="cdf5c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cdf5c-135">System.String</span></span>

## <span data-ttu-id="cdf5c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdf5c-136">OUTPUTS</span></span>

### <span data-ttu-id="cdf5c-137">System. void</span><span class="sxs-lookup"><span data-stu-id="cdf5c-137">System.Void</span></span>

## <span data-ttu-id="cdf5c-138">Note</span><span class="sxs-lookup"><span data-stu-id="cdf5c-138">NOTES</span></span>

## <span data-ttu-id="cdf5c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdf5c-139">RELATED LINKS</span></span>

[<span data-ttu-id="cdf5c-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdf5c-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="cdf5c-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdf5c-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="cdf5c-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cdf5c-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


