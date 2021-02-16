---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187551"
---
# <span data-ttu-id="e984e-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="e984e-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="e984e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e984e-102">SYNOPSIS</span></span>
<span data-ttu-id="e984e-103">Aggiorna l'account di integrazione ricevuto come numero di controllo interscambio (ICN) nel gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="e984e-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="e984e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e984e-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e984e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e984e-105">DESCRIPTION</span></span>
<span data-ttu-id="e984e-106">Il Set-AzIntegrationAccountGeneratedIcn cmdlet aggiorna un account di integrazione esistente che ha ricevuto il numero di controllo di interscambio (ICN) e restituisce un oggetto che rappresenta il numero di controllo dell'interscambio ricevuto dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e984e-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="e984e-107">Usare questo cmdlet per aggiornare lo stato di elaborazione dei messaggi di un account di integrazione ricevuto dal numero di controllo interscambio.</span><span class="sxs-lookup"><span data-stu-id="e984e-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="e984e-108">È possibile aggiornare un account di integrazione ricevuto tramite interscambio specificando il nome dell'account di integrazione, il nome del gruppo di risorse, il nome del contratto, il valore del numero di controllo e lo stato di elaborazione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="e984e-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="e984e-109">Non è possibile creare un nuovo account di integrazione ricevuto con questo comando.</span><span class="sxs-lookup"><span data-stu-id="e984e-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="e984e-110">Per usare i parametri dinamici, è sufficiente digitarli nel comando oppure digitare un segno meno (-) per indicare il nome di un parametro e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="e984e-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e984e-111">Se non si specifica un parametro del modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="e984e-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="e984e-112">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri di modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="e984e-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="e984e-113">Specifica il parametro "-AgreementType" per specificare se i numeri di controllo X12 o Edifact devono restituire</span><span class="sxs-lookup"><span data-stu-id="e984e-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="e984e-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e984e-114">EXAMPLES</span></span>

### <span data-ttu-id="e984e-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e984e-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="e984e-116">Questo comando aggiorna il numero di controllo interscambio X12 ricevuto dall'account di integrazione per uno specifico contratto per l'account di integrazione e il valore con lo stato di elaborazione dei messaggi non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e984e-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="e984e-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e984e-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="e984e-118">Questo comando aggiorna il numero di controllo interscambio Edifact ricevuto dall'account di integrazione per uno specifico contratto di account di integrazione e il valore con lo stato di elaborazione dei messaggi non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e984e-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="e984e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e984e-119">PARAMETERS</span></span>

### <span data-ttu-id="e984e-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="e984e-120">-AgreementName</span></span>
<span data-ttu-id="e984e-121">Nome del contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e984e-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="e984e-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="e984e-122">-AgreementType</span></span>
<span data-ttu-id="e984e-123">Il tipo di contratto dell'account di integrazione (X12 o Edifact).</span><span class="sxs-lookup"><span data-stu-id="e984e-123">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e984e-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="e984e-124">-ControlNumberValue</span></span>
<span data-ttu-id="e984e-125">Valore numerico di controllo dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e984e-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="e984e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e984e-126">-DefaultProfile</span></span>
<span data-ttu-id="e984e-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e984e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e984e-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="e984e-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="e984e-129">Stato di elaborazione dei messaggi ricevuti.</span><span class="sxs-lookup"><span data-stu-id="e984e-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e984e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e984e-130">-Name</span></span>
<span data-ttu-id="e984e-131">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e984e-131">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e984e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e984e-132">-ResourceGroupName</span></span>
<span data-ttu-id="e984e-133">Nome del gruppo di risorse dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e984e-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="e984e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e984e-134">-Confirm</span></span>
<span data-ttu-id="e984e-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e984e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e984e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e984e-136">-WhatIf</span></span>
<span data-ttu-id="e984e-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e984e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e984e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e984e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e984e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e984e-139">CommonParameters</span></span>
<span data-ttu-id="e984e-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e984e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e984e-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e984e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e984e-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="e984e-142">INPUTS</span></span>

### <span data-ttu-id="e984e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e984e-143">System.String</span></span>

## <span data-ttu-id="e984e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e984e-144">OUTPUTS</span></span>

### <span data-ttu-id="e984e-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="e984e-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="e984e-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="e984e-146">NOTES</span></span>

## <span data-ttu-id="e984e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e984e-147">RELATED LINKS</span></span>

<span data-ttu-id="e984e-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="e984e-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
