---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: df7266548b616615fa45131c21f40622894ffe9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960574"
---
# <span data-ttu-id="57393-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="57393-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="57393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57393-102">SYNOPSIS</span></span>
<span data-ttu-id="57393-103">Questo cmdlet recupera un numero di controllo interscambio ricevuto specifico per contratto e valore di numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="57393-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="57393-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57393-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57393-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="57393-105">DESCRIPTION</span></span>
<span data-ttu-id="57393-106">Questo cmdlet è destinato a essere usato in scenari di ripristino di emergenza per convalidare la presenza di un numero di controllo interscambio ricevuto e facoltativamente per rimuovere tale entità con Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="57393-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="57393-107">Specifica il parametro "-AgreementType" per specificare se i numeri di controllo X12 o Edifact devono restituire</span><span class="sxs-lookup"><span data-stu-id="57393-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="57393-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57393-108">EXAMPLES</span></span>

### <span data-ttu-id="57393-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57393-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="57393-110">Questo comando recupera il numero di controllo interscambio ricevuto dall'account di integrazione X12 in base al nome del contratto e al valore del numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="57393-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="57393-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="57393-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="57393-112">Questo comando recupera il numero di controllo interscambio ricevuto dall'account di integrazione Edifact in base al nome del contratto e al valore del numero di controllo.</span><span class="sxs-lookup"><span data-stu-id="57393-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="57393-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57393-113">PARAMETERS</span></span>

### <span data-ttu-id="57393-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="57393-114">-AgreementName</span></span>
<span data-ttu-id="57393-115">Nome del contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="57393-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="57393-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="57393-116">-AgreementType</span></span>
<span data-ttu-id="57393-117">Tipo di contratto dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="57393-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="57393-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="57393-118">-ControlNumberValue</span></span>
<span data-ttu-id="57393-119">Valore numerico di controllo dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="57393-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="57393-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57393-120">-DefaultProfile</span></span>
<span data-ttu-id="57393-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="57393-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57393-122">-Name</span><span class="sxs-lookup"><span data-stu-id="57393-122">-Name</span></span>
<span data-ttu-id="57393-123">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="57393-123">The integration account name.</span></span>

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

### <span data-ttu-id="57393-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57393-124">-ResourceGroupName</span></span>
<span data-ttu-id="57393-125">Nome del gruppo di risorse dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="57393-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="57393-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57393-126">CommonParameters</span></span>
<span data-ttu-id="57393-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57393-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57393-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57393-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57393-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="57393-129">INPUTS</span></span>

### <span data-ttu-id="57393-130">System.String</span><span class="sxs-lookup"><span data-stu-id="57393-130">System.String</span></span>

## <span data-ttu-id="57393-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57393-131">OUTPUTS</span></span>

### <span data-ttu-id="57393-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="57393-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="57393-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="57393-133">NOTES</span></span>

## <span data-ttu-id="57393-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57393-134">RELATED LINKS</span></span>

[<span data-ttu-id="57393-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="57393-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="57393-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="57393-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
