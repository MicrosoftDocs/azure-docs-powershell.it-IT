---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b6bf2c126a1009d824ab8bae1ea2e2031459d876
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960606"
---
# <span data-ttu-id="1a351-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="1a351-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="1a351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a351-102">SYNOPSIS</span></span>
<span data-ttu-id="1a351-103">Questo cmdlet recupera il valore corrente del numero di controllo interscambio generato in base al contratto.</span><span class="sxs-lookup"><span data-stu-id="1a351-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="1a351-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a351-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a351-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a351-105">DESCRIPTION</span></span>
<span data-ttu-id="1a351-106">Questo cmdlet è destinato a essere usato in scenari di ripristino di emergenza per recuperare il valore corrente del numero di controllo interscambio generato in modo da scrivere un valore maggiore con Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="1a351-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="1a351-107">Il numero di controllo dell'interscambio deve essere aumentato per evitare numeri di controllo interscambio duplicati per i numeri che non potevano ancora essere replicati nell'area passiva in caso di emergenza nell'area attiva.</span><span class="sxs-lookup"><span data-stu-id="1a351-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="1a351-108">Specifica il parametro "-AgreementType" per specificare se i numeri di controllo X12 o Edifact devono restituire</span><span class="sxs-lookup"><span data-stu-id="1a351-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="1a351-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a351-109">EXAMPLES</span></span>

### <span data-ttu-id="1a351-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a351-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="1a351-111">Questo comando recupera il numero di controllo interscambio X12 generato dall'account di integrazione in base al nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="1a351-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="1a351-112">Verificare che il contratto specificato sia di tipo "X12"</span><span class="sxs-lookup"><span data-stu-id="1a351-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="1a351-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1a351-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="1a351-114">Questo comando recupera il numero di controllo interscambio Edifact generato dall'account di integrazione in base al nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="1a351-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="1a351-115">Verificare che il contratto specificato sia di tipo "Edifact"</span><span class="sxs-lookup"><span data-stu-id="1a351-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="1a351-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1a351-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="1a351-117">Questo comando recupera tutti i numeri di controllo interscambio X12 generati in base al nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1a351-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="1a351-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a351-118">PARAMETERS</span></span>

### <span data-ttu-id="1a351-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="1a351-119">-AgreementName</span></span>
<span data-ttu-id="1a351-120">Nome del contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1a351-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a351-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="1a351-121">-AgreementType</span></span>
<span data-ttu-id="1a351-122">Tipo di contratto dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1a351-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="1a351-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a351-123">-DefaultProfile</span></span>
<span data-ttu-id="1a351-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1a351-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a351-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1a351-125">-Name</span></span>
<span data-ttu-id="1a351-126">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1a351-126">The integration account name.</span></span>

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

### <span data-ttu-id="1a351-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a351-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a351-128">Nome del gruppo di risorse dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1a351-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="1a351-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a351-129">CommonParameters</span></span>
<span data-ttu-id="1a351-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a351-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a351-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a351-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a351-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a351-132">INPUTS</span></span>

### <span data-ttu-id="1a351-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1a351-133">System.String</span></span>

## <span data-ttu-id="1a351-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a351-134">OUTPUTS</span></span>

### <span data-ttu-id="1a351-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="1a351-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="1a351-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a351-136">NOTES</span></span>

## <span data-ttu-id="1a351-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a351-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a351-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="1a351-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

