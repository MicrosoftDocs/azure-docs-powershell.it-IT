---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487183"
---
# <span data-ttu-id="6de26-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6de26-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="6de26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6de26-102">SYNOPSIS</span></span>
<span data-ttu-id="6de26-103">Crea un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6de26-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="6de26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6de26-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6de26-105">DESCRIPTION</span></span>
<span data-ttu-id="6de26-106">Il cmdlet **New-AzIntegrationAccountAgreement** crea un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6de26-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="6de26-107">Questo cmdlet restituisce un oggetto che rappresenta il contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="6de26-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="6de26-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome dell'accordo, il tipo, il nome del partner, i qualificatori partner e il contenuto del contratto</span><span class="sxs-lookup"><span data-stu-id="6de26-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="6de26-109">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="6de26-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="6de26-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="6de26-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6de26-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="6de26-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6de26-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="6de26-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6de26-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="6de26-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6de26-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6de26-114">EXAMPLES</span></span>

### <span data-ttu-id="6de26-115">Esempio 1: creare un contratto per l'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="6de26-115">Example 1: Create a integration account agreement</span></span>
```powershell
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="6de26-116">Questo comando crea un contratto per l'account di integrazione nel gruppo di risorse Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="6de26-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="6de26-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6de26-117">Example 2</span></span>

<span data-ttu-id="6de26-118">Crea un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6de26-118">Creates an integration account agreement.</span></span> <span data-ttu-id="6de26-119">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6de26-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="6de26-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6de26-120">PARAMETERS</span></span>

### <span data-ttu-id="6de26-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="6de26-121">-AgreementContent</span></span>
<span data-ttu-id="6de26-122">Specifica il contenuto del contratto, in formato JSON (JavaScript Object Notation) per il contratto.</span><span class="sxs-lookup"><span data-stu-id="6de26-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="6de26-123">Specificare questo parametro o il parametro *AgreementContentFilePath* .</span><span class="sxs-lookup"><span data-stu-id="6de26-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="6de26-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="6de26-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="6de26-125">Specifica il percorso del file del contenuto del contratto per il contratto.</span><span class="sxs-lookup"><span data-stu-id="6de26-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="6de26-126">Specificare questo parametro o il parametro *AgreementContent* .</span><span class="sxs-lookup"><span data-stu-id="6de26-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="6de26-127">-Contratto</span><span class="sxs-lookup"><span data-stu-id="6de26-127">-AgreementName</span></span>
<span data-ttu-id="6de26-128">Specifica un nome per il contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="6de26-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="6de26-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="6de26-129">-AgreementType</span></span>
<span data-ttu-id="6de26-130">Specifica il tipo di contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6de26-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="6de26-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6de26-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6de26-132">X12</span><span class="sxs-lookup"><span data-stu-id="6de26-132">X12</span></span> 
- <span data-ttu-id="6de26-133">AS2</span><span class="sxs-lookup"><span data-stu-id="6de26-133">AS2</span></span>
- <span data-ttu-id="6de26-134">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="6de26-134">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de26-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de26-135">-DefaultProfile</span></span>
<span data-ttu-id="6de26-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6de26-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6de26-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="6de26-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="6de26-138">Specifica un qualificatore di identità aziendale per il partner guest.</span><span class="sxs-lookup"><span data-stu-id="6de26-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="6de26-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="6de26-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="6de26-140">Il valore del qualificatore dell'identità Guest Integration Agreement.</span><span class="sxs-lookup"><span data-stu-id="6de26-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="6de26-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="6de26-141">-GuestPartner</span></span>
<span data-ttu-id="6de26-142">Specifica il nome del partner guest.</span><span class="sxs-lookup"><span data-stu-id="6de26-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="6de26-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="6de26-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="6de26-144">Specifica un qualificatore di identità aziendale per il partner host.</span><span class="sxs-lookup"><span data-stu-id="6de26-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="6de26-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="6de26-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="6de26-146">Valore del qualificatore dell'identità host del contratto di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6de26-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="6de26-147">-Capofila Segds</span><span class="sxs-lookup"><span data-stu-id="6de26-147">-HostPartner</span></span>
<span data-ttu-id="6de26-148">Specifica il nome del partner host.</span><span class="sxs-lookup"><span data-stu-id="6de26-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="6de26-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6de26-149">-Metadata</span></span>
<span data-ttu-id="6de26-150">Specifica un oggetto Metadata per il contratto.</span><span class="sxs-lookup"><span data-stu-id="6de26-150">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de26-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="6de26-151">-Name</span></span>
<span data-ttu-id="6de26-152">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6de26-152">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6de26-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de26-153">-ResourceGroupName</span></span>
<span data-ttu-id="6de26-154">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6de26-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6de26-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6de26-155">-Confirm</span></span>
<span data-ttu-id="6de26-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6de26-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de26-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de26-157">-WhatIf</span></span>
<span data-ttu-id="6de26-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6de26-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de26-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6de26-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de26-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de26-160">CommonParameters</span></span>
<span data-ttu-id="6de26-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de26-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de26-162">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de26-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de26-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6de26-163">INPUTS</span></span>

### <span data-ttu-id="6de26-164">System. String</span><span class="sxs-lookup"><span data-stu-id="6de26-164">System.String</span></span>

## <span data-ttu-id="6de26-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6de26-165">OUTPUTS</span></span>

### <span data-ttu-id="6de26-166">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6de26-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="6de26-167">Note</span><span class="sxs-lookup"><span data-stu-id="6de26-167">NOTES</span></span>

## <span data-ttu-id="6de26-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6de26-168">RELATED LINKS</span></span>

[<span data-ttu-id="6de26-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6de26-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6de26-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6de26-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6de26-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6de26-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


