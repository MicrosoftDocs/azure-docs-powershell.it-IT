---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345967"
---
# <span data-ttu-id="d2512-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d2512-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="d2512-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2512-102">SYNOPSIS</span></span>
<span data-ttu-id="d2512-103">Rimuove un partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d2512-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="d2512-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2512-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2512-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2512-105">DESCRIPTION</span></span>
<span data-ttu-id="d2512-106">Il cmdlet **Remove-AzIntegrationAccountPartner** rimuove un partner dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d2512-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="d2512-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="d2512-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="d2512-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="d2512-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d2512-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="d2512-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d2512-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d2512-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d2512-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="d2512-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d2512-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2512-112">EXAMPLES</span></span>

### <span data-ttu-id="d2512-113">Esempio 1: rimuovere un partner dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="d2512-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="d2512-114">Questo comando rimuove il partner account di integrazione denominato IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="d2512-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="d2512-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2512-115">PARAMETERS</span></span>

### <span data-ttu-id="d2512-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2512-116">-DefaultProfile</span></span>
<span data-ttu-id="d2512-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d2512-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2512-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d2512-118">-Force</span></span>
<span data-ttu-id="d2512-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d2512-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2512-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2512-120">-Name</span></span>
<span data-ttu-id="d2512-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d2512-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d2512-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="d2512-122">-PartnerName</span></span>
<span data-ttu-id="d2512-123">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="d2512-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="d2512-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2512-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2512-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d2512-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2512-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2512-126">-Confirm</span></span>
<span data-ttu-id="d2512-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2512-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2512-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2512-128">-WhatIf</span></span>
<span data-ttu-id="d2512-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2512-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2512-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2512-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2512-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2512-131">CommonParameters</span></span>
<span data-ttu-id="d2512-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2512-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2512-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2512-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2512-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2512-134">INPUTS</span></span>

### <span data-ttu-id="d2512-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d2512-135">System.String</span></span>

## <span data-ttu-id="d2512-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2512-136">OUTPUTS</span></span>

### <span data-ttu-id="d2512-137">System. void</span><span class="sxs-lookup"><span data-stu-id="d2512-137">System.Void</span></span>

## <span data-ttu-id="d2512-138">Note</span><span class="sxs-lookup"><span data-stu-id="d2512-138">NOTES</span></span>

## <span data-ttu-id="d2512-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2512-139">RELATED LINKS</span></span>

[<span data-ttu-id="d2512-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d2512-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="d2512-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d2512-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="d2512-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d2512-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


