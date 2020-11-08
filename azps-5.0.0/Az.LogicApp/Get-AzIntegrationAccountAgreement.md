---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 46cc7c75075cffface03af2ed70b5339dd36b0a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201175"
---
# <span data-ttu-id="c882a-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c882a-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="c882a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c882a-102">SYNOPSIS</span></span>
<span data-ttu-id="c882a-103">Ottiene un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c882a-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="c882a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c882a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c882a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c882a-105">DESCRIPTION</span></span>
<span data-ttu-id="c882a-106">Il cmdlet **Get-AzIntegrationAccountAgreement** ottiene un contratto di integrazione di un account da un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c882a-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="c882a-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="c882a-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="c882a-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="c882a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c882a-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="c882a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c882a-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="c882a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c882a-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="c882a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c882a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c882a-112">EXAMPLES</span></span>

### <span data-ttu-id="c882a-113">Esempio 1: ottenere un contratto per l'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="c882a-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="c882a-114">Questo comando ottiene un contratto per l'account di integrazione denominato IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="c882a-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="c882a-115">Esempio 2: ottenere gli accordi per l'account di integrazione per nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c882a-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="c882a-116">Questo comando ottiene il nome del gruppo di risorse per i contratti di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="c882a-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="c882a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c882a-117">PARAMETERS</span></span>

### <span data-ttu-id="c882a-118">-Contratto</span><span class="sxs-lookup"><span data-stu-id="c882a-118">-AgreementName</span></span>
<span data-ttu-id="c882a-119">Specifica il nome di un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c882a-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="c882a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c882a-120">-DefaultProfile</span></span>
<span data-ttu-id="c882a-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c882a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c882a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c882a-122">-Name</span></span>
<span data-ttu-id="c882a-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c882a-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c882a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c882a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c882a-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c882a-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c882a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c882a-126">CommonParameters</span></span>
<span data-ttu-id="c882a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c882a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c882a-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c882a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c882a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c882a-129">INPUTS</span></span>

### <span data-ttu-id="c882a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c882a-130">System.String</span></span>

## <span data-ttu-id="c882a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c882a-131">OUTPUTS</span></span>

### <span data-ttu-id="c882a-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c882a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="c882a-133">Note</span><span class="sxs-lookup"><span data-stu-id="c882a-133">NOTES</span></span>

## <span data-ttu-id="c882a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c882a-134">RELATED LINKS</span></span>

[<span data-ttu-id="c882a-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c882a-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="c882a-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c882a-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="c882a-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="c882a-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


