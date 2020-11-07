---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 94cb9c54752b29da68beefa713894fd77a385b45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673964"
---
# <span data-ttu-id="90146-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="90146-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="90146-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90146-102">SYNOPSIS</span></span>
<span data-ttu-id="90146-103">Aggiorna il numero di controllo dell'interscambio (ICN) ricevuto dell'account di integrazione nel gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="90146-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="90146-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90146-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90146-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90146-105">DESCRIPTION</span></span>
<span data-ttu-id="90146-106">Il cmdlet Set-AzIntegrationAccountGeneratedIcn aggiorna un numero di controllo interscambio ricevuto (ICN) di un account di integrazione esistente e restituisce un oggetto che rappresenta il numero di controllo dell'interscambio ricevuto dall'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="90146-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="90146-107">Questo cmdlet consente di aggiornare lo stato di elaborazione dei messaggi del numero di controllo interscambio ricevuto dall'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="90146-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="90146-108">È possibile aggiornare un numero di controllo dell'interscambio ricevuto dall'account di integrazione specificando il nome dell'account di integrazione, il nome del gruppo di risorse, il nome del contratto, il valore del numero di controllo e lo stato</span><span class="sxs-lookup"><span data-stu-id="90146-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="90146-109">Non è possibile creare un nuovo account di integrazione ricevuto numero di controllo interscambio con questo comando.</span><span class="sxs-lookup"><span data-stu-id="90146-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="90146-110">Per usare i parametri dinamici, è sufficiente digitarli nel comando oppure digitare un segno meno (-) per indicare il nome di un parametro e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="90146-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="90146-111">Se si dimentica un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="90146-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="90146-112">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="90146-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="90146-113">Fornisci il parametro "-AgreementType" per specificare se i numeri di controllo X12 o EDIFACT restituiscono</span><span class="sxs-lookup"><span data-stu-id="90146-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="90146-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90146-114">EXAMPLES</span></span>

### <span data-ttu-id="90146-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90146-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="90146-116">Questo comando Aggiorna l'account di integrazione ricevuto il numero di controllo interscambio X12 per un contratto specifico di integrazione e un valore con lo stato di elaborazione dei messaggi non riuscito.</span><span class="sxs-lookup"><span data-stu-id="90146-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="90146-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="90146-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="90146-118">Questo comando Aggiorna l'account di integrazione che ha ricevuto il numero di controllo interscambio EDIFACT per un contratto specifico di integrazione e un valore con lo stato di elaborazione dei messaggi non riuscito.</span><span class="sxs-lookup"><span data-stu-id="90146-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="90146-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90146-119">PARAMETERS</span></span>

### <span data-ttu-id="90146-120">-Contratto</span><span class="sxs-lookup"><span data-stu-id="90146-120">-AgreementName</span></span>
<span data-ttu-id="90146-121">Nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="90146-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="90146-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="90146-122">-AgreementType</span></span>
<span data-ttu-id="90146-123">Tipo di contratto per l'account di integrazione (X12 o EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="90146-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="90146-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="90146-124">-ControlNumberValue</span></span>
<span data-ttu-id="90146-125">Valore del numero di controllo dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="90146-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="90146-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90146-126">-DefaultProfile</span></span>
<span data-ttu-id="90146-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="90146-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90146-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="90146-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="90146-129">Stato di elaborazione dei messaggi ricevuti.</span><span class="sxs-lookup"><span data-stu-id="90146-129">The received message processing status.</span></span>

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

### <span data-ttu-id="90146-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="90146-130">-Name</span></span>
<span data-ttu-id="90146-131">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="90146-131">The integration account name.</span></span>

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

### <span data-ttu-id="90146-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90146-132">-ResourceGroupName</span></span>
<span data-ttu-id="90146-133">Nome del gruppo risorse account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="90146-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="90146-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90146-134">-Confirm</span></span>
<span data-ttu-id="90146-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90146-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90146-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90146-136">-WhatIf</span></span>
<span data-ttu-id="90146-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90146-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90146-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90146-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90146-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90146-139">CommonParameters</span></span>
<span data-ttu-id="90146-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90146-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90146-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90146-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90146-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90146-142">INPUTS</span></span>

### <span data-ttu-id="90146-143">System. String</span><span class="sxs-lookup"><span data-stu-id="90146-143">System.String</span></span>

## <span data-ttu-id="90146-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90146-144">OUTPUTS</span></span>

### <span data-ttu-id="90146-145">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="90146-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="90146-146">Note</span><span class="sxs-lookup"><span data-stu-id="90146-146">NOTES</span></span>

## <span data-ttu-id="90146-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90146-147">RELATED LINKS</span></span>

<span data-ttu-id="90146-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="90146-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
