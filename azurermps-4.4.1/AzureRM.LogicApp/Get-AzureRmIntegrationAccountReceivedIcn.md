---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: be42bd7d3e4a6a839182ae36d71f73377460eceb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510532"
---
# <span data-ttu-id="cc39b-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="cc39b-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="cc39b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc39b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc39b-103">Questo cmdlet recupera un numero di controllo di interscambio ricevuto specifico per contratto e valore numerico di controllo.</span><span class="sxs-lookup"><span data-stu-id="cc39b-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc39b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc39b-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc39b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc39b-105">DESCRIPTION</span></span>
<span data-ttu-id="cc39b-106">Questo cmdlet deve essere usato negli scenari di ripristino di emergenza per convalidare la presenza di un numero di controllo interscambio ricevuto e facoltativamente per rimuovere tale entità con Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="cc39b-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="cc39b-107">Fornisci il parametro "-AgreementType" per specificare se i numeri di controllo X12 o EDIFACT restituiscono</span><span class="sxs-lookup"><span data-stu-id="cc39b-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="cc39b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc39b-108">EXAMPLES</span></span>

### <span data-ttu-id="cc39b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cc39b-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="cc39b-110">Questo comando ottiene il numero di controllo dell'interscambio ricevuto dall'account di integrazione X12 in base al nome e al valore del numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="cc39b-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="cc39b-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cc39b-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="cc39b-112">Questo comando ottiene il numero di controllo dell'interscambio ricevuto dall'account di integrazione EDIFACT in base al nome e al valore del numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="cc39b-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="cc39b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc39b-113">PARAMETERS</span></span>

### <span data-ttu-id="cc39b-114">-Contratto</span><span class="sxs-lookup"><span data-stu-id="cc39b-114">-AgreementName</span></span>
<span data-ttu-id="cc39b-115">Nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="cc39b-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="cc39b-116">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="cc39b-116">-ControlNumberValue</span></span>
<span data-ttu-id="cc39b-117">Valore del numero di controllo dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc39b-117">The integration account control number value.</span></span>

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

### <span data-ttu-id="cc39b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc39b-118">-Name</span></span>
<span data-ttu-id="cc39b-119">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc39b-119">The integration account name.</span></span>

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

### <span data-ttu-id="cc39b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc39b-120">-ResourceGroupName</span></span>
<span data-ttu-id="cc39b-121">Nome del gruppo risorse account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc39b-121">The integration account resource group name.</span></span>

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

### <span data-ttu-id="cc39b-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="cc39b-122">-AgreementType</span></span>
<span data-ttu-id="cc39b-123">Tipo di contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cc39b-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc39b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc39b-124">-DefaultProfile</span></span>
<span data-ttu-id="cc39b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc39b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc39b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc39b-126">CommonParameters</span></span>
<span data-ttu-id="cc39b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc39b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc39b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc39b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc39b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc39b-129">INPUTS</span></span>

### <span data-ttu-id="cc39b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cc39b-130">System.String</span></span>

## <span data-ttu-id="cc39b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc39b-131">OUTPUTS</span></span>

### <span data-ttu-id="cc39b-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="cc39b-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="cc39b-133">Note</span><span class="sxs-lookup"><span data-stu-id="cc39b-133">NOTES</span></span>

## <span data-ttu-id="cc39b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc39b-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc39b-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="cc39b-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="cc39b-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="cc39b-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
