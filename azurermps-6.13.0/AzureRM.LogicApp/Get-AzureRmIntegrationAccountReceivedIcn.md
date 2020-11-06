---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: b9defadc92619d136c82302203d296d6b71318ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513783"
---
# <span data-ttu-id="9391c-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="9391c-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="9391c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9391c-102">SYNOPSIS</span></span>
<span data-ttu-id="9391c-103">Questo cmdlet recupera un numero di controllo di interscambio ricevuto specifico per contratto e valore numerico di controllo.</span><span class="sxs-lookup"><span data-stu-id="9391c-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9391c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9391c-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9391c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9391c-105">DESCRIPTION</span></span>
<span data-ttu-id="9391c-106">Questo cmdlet deve essere usato negli scenari di ripristino di emergenza per convalidare la presenza di un numero di controllo interscambio ricevuto e facoltativamente per rimuovere tale entità con Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="9391c-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="9391c-107">Fornisci il parametro "-AgreementType" per specificare se i numeri di controllo X12 o EDIFACT restituiscono</span><span class="sxs-lookup"><span data-stu-id="9391c-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="9391c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9391c-108">EXAMPLES</span></span>

### <span data-ttu-id="9391c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9391c-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="9391c-110">Questo comando ottiene il numero di controllo dell'interscambio ricevuto dall'account di integrazione X12 in base al nome e al valore del numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="9391c-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="9391c-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9391c-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="9391c-112">Questo comando ottiene il numero di controllo dell'interscambio ricevuto dall'account di integrazione EDIFACT in base al nome e al valore del numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="9391c-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="9391c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9391c-113">PARAMETERS</span></span>

### <span data-ttu-id="9391c-114">-Contratto</span><span class="sxs-lookup"><span data-stu-id="9391c-114">-AgreementName</span></span>
<span data-ttu-id="9391c-115">Nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="9391c-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="9391c-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="9391c-116">-AgreementType</span></span>
<span data-ttu-id="9391c-117">Tipo di contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9391c-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="9391c-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="9391c-118">-ControlNumberValue</span></span>
<span data-ttu-id="9391c-119">Valore del numero di controllo dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9391c-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="9391c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9391c-120">-DefaultProfile</span></span>
<span data-ttu-id="9391c-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9391c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9391c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9391c-122">-Name</span></span>
<span data-ttu-id="9391c-123">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9391c-123">The integration account name.</span></span>

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

### <span data-ttu-id="9391c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9391c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9391c-125">Nome del gruppo risorse account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9391c-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="9391c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9391c-126">CommonParameters</span></span>
<span data-ttu-id="9391c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9391c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9391c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9391c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9391c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9391c-129">INPUTS</span></span>

### <span data-ttu-id="9391c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9391c-130">System.String</span></span>

## <span data-ttu-id="9391c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9391c-131">OUTPUTS</span></span>

### <span data-ttu-id="9391c-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="9391c-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="9391c-133">Note</span><span class="sxs-lookup"><span data-stu-id="9391c-133">NOTES</span></span>

## <span data-ttu-id="9391c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9391c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9391c-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="9391c-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="9391c-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="9391c-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
