---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 971e96b61b22bd5efbd22b82468d864a63392a16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835515"
---
# <span data-ttu-id="8646d-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8646d-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="8646d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8646d-102">SYNOPSIS</span></span>
<span data-ttu-id="8646d-103">Questo cmdlet recupera il valore corrente del numero di controllo interscambio generato per contratto.</span><span class="sxs-lookup"><span data-stu-id="8646d-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="8646d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8646d-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8646d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8646d-105">DESCRIPTION</span></span>
<span data-ttu-id="8646d-106">Questo cmdlet deve essere usato negli scenari di ripristino di emergenza per recuperare il valore corrente del numero di controllo interscambio generato in modo da restituire un valore aumentato con set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="8646d-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="8646d-107">Il numero di controllo interscambio deve essere aumentato per evitare numeri di controllo interscambio duplicati per i numeri che non sono stati ancora replicati nell'area passiva quando il disastro è avvenuto nell'area attiva.</span><span class="sxs-lookup"><span data-stu-id="8646d-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="8646d-108">Fornisci il parametro "-AgreementType" per specificare se i numeri di controllo X12 o EDIFACT restituiscono</span><span class="sxs-lookup"><span data-stu-id="8646d-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="8646d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8646d-109">EXAMPLES</span></span>

### <span data-ttu-id="8646d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8646d-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8646d-111">Questo comando consente di ottenere il numero di controllo dell'interscambio X12 generato dall'account in base al nome dell'accordo.</span><span class="sxs-lookup"><span data-stu-id="8646d-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="8646d-112">Verificare che il contratto specificato sia di tipo "X12"</span><span class="sxs-lookup"><span data-stu-id="8646d-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="8646d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8646d-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8646d-114">Questo comando ottiene il numero di controllo di interscambio EDIFACT generato dall'account di integrazione per nome contratto.</span><span class="sxs-lookup"><span data-stu-id="8646d-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="8646d-115">Verificare che l'accordo specificato sia di tipo "EDIFACT"</span><span class="sxs-lookup"><span data-stu-id="8646d-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="8646d-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8646d-116">Example 3</span></span>
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

<span data-ttu-id="8646d-117">Questo comando ottiene tutti i numeri di controllo interscambio X12 generati tramite il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8646d-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="8646d-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8646d-118">PARAMETERS</span></span>

### <span data-ttu-id="8646d-119">-Contratto</span><span class="sxs-lookup"><span data-stu-id="8646d-119">-AgreementName</span></span>
<span data-ttu-id="8646d-120">Nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="8646d-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="8646d-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="8646d-121">-AgreementType</span></span>
<span data-ttu-id="8646d-122">Tipo di contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8646d-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="8646d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8646d-123">-DefaultProfile</span></span>
<span data-ttu-id="8646d-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8646d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8646d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8646d-125">-Name</span></span>
<span data-ttu-id="8646d-126">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8646d-126">The integration account name.</span></span>

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

### <span data-ttu-id="8646d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8646d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8646d-128">Nome del gruppo risorse account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8646d-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="8646d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8646d-129">CommonParameters</span></span>
<span data-ttu-id="8646d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8646d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8646d-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8646d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8646d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8646d-132">INPUTS</span></span>

### <span data-ttu-id="8646d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8646d-133">System.String</span></span>

## <span data-ttu-id="8646d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8646d-134">OUTPUTS</span></span>

### <span data-ttu-id="8646d-135">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="8646d-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="8646d-136">Note</span><span class="sxs-lookup"><span data-stu-id="8646d-136">NOTES</span></span>

## <span data-ttu-id="8646d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8646d-137">RELATED LINKS</span></span>

[<span data-ttu-id="8646d-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8646d-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

