---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 416a5991be227364e4374d3e4c0e64caa3095b9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673987"
---
# <span data-ttu-id="326a9-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="326a9-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="326a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="326a9-102">SYNOPSIS</span></span>
<span data-ttu-id="326a9-103">Questo cmdlet rimuove un numero di controllo di interscambio ricevuto specifico per contratto e valore numerico di controllo.</span><span class="sxs-lookup"><span data-stu-id="326a9-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="326a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="326a9-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="326a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="326a9-105">DESCRIPTION</span></span>
<span data-ttu-id="326a9-106">Questo cmdlet deve essere usato negli scenari di ripristino di emergenza per rimuovere un numero di controllo interscambio ricevuto dall'account di integrazione in modo che il connettore B2B possa rielaborare il messaggio quando è abilitato il rilevamento dei numeri duplicati.</span><span class="sxs-lookup"><span data-stu-id="326a9-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="326a9-107">In rare occasioni, il numero di controllo dell'interscambio ricevuto può essere prenotato poco prima di un disastro e prima che il connettore B2B rigetti l'interscambio come errato.</span><span class="sxs-lookup"><span data-stu-id="326a9-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="326a9-108">In tali occasioni l'operazione potrebbe voler consentire al sito di ripristino di elaborare di nuovo lo stesso interscambio dopo la correzione del payload.</span><span class="sxs-lookup"><span data-stu-id="326a9-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="326a9-109">Fornisci il parametro "-AgreementType" per specificare se i numeri di controllo X12 o EDIFACT restituiscono</span><span class="sxs-lookup"><span data-stu-id="326a9-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="326a9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="326a9-110">EXAMPLES</span></span>

### <span data-ttu-id="326a9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="326a9-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="326a9-112">Cerca di ottenere un numero di controllo di interscambio X12 ricevuto che il contenuto non è in un formato valido.</span><span class="sxs-lookup"><span data-stu-id="326a9-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="326a9-113">Rimuove il numero di controllo interscambio X12 ricevuto.</span><span class="sxs-lookup"><span data-stu-id="326a9-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="326a9-114">Conferma che il numero di controllo interscambio X12 ricevuto è stato rimosso provando a recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="326a9-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="326a9-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="326a9-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="326a9-116">Cerca di ottenere un numero di controllo di interscambio EDIFACT ricevuto che il contenuto non è in un formato valido.</span><span class="sxs-lookup"><span data-stu-id="326a9-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="326a9-117">Rimuove il numero di controllo dell'interscambio EDIFACT ricevuto.</span><span class="sxs-lookup"><span data-stu-id="326a9-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="326a9-118">Conferma che il numero di controllo dell'interscambio EDIFACT ricevuto è stato rimosso provando a recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="326a9-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="326a9-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="326a9-119">PARAMETERS</span></span>

### <span data-ttu-id="326a9-120">-Contratto</span><span class="sxs-lookup"><span data-stu-id="326a9-120">-AgreementName</span></span>
<span data-ttu-id="326a9-121">Nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="326a9-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="326a9-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="326a9-122">-AgreementType</span></span>
<span data-ttu-id="326a9-123">Tipo di contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="326a9-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="326a9-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="326a9-124">-ControlNumberValue</span></span>
<span data-ttu-id="326a9-125">Valore del numero di controllo dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="326a9-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="326a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326a9-126">-DefaultProfile</span></span>
<span data-ttu-id="326a9-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="326a9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="326a9-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="326a9-128">-Name</span></span>
<span data-ttu-id="326a9-129">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="326a9-129">The integration account name.</span></span>

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

### <span data-ttu-id="326a9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326a9-130">-ResourceGroupName</span></span>
<span data-ttu-id="326a9-131">Nome del gruppo risorse account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="326a9-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="326a9-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="326a9-132">-Confirm</span></span>
<span data-ttu-id="326a9-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="326a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="326a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="326a9-134">-WhatIf</span></span>
<span data-ttu-id="326a9-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="326a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="326a9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="326a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="326a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326a9-137">CommonParameters</span></span>
<span data-ttu-id="326a9-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326a9-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326a9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326a9-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="326a9-140">INPUTS</span></span>

### <span data-ttu-id="326a9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="326a9-141">System.String</span></span>

## <span data-ttu-id="326a9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="326a9-142">OUTPUTS</span></span>

### <span data-ttu-id="326a9-143">System. void</span><span class="sxs-lookup"><span data-stu-id="326a9-143">System.Void</span></span>

## <span data-ttu-id="326a9-144">Note</span><span class="sxs-lookup"><span data-stu-id="326a9-144">NOTES</span></span>

## <span data-ttu-id="326a9-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="326a9-145">RELATED LINKS</span></span>

<span data-ttu-id="326a9-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="326a9-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

