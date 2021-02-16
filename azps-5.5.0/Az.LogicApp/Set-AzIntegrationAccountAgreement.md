---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ac0e5e89706e648d714e3f09ebad5dee7d7b4416
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180359"
---
# <span data-ttu-id="b0255-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b0255-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="b0255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0255-102">SYNOPSIS</span></span>
<span data-ttu-id="b0255-103">Modifica un contratto di integrazione con l'account.</span><span class="sxs-lookup"><span data-stu-id="b0255-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="b0255-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0255-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0255-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0255-105">DESCRIPTION</span></span>
<span data-ttu-id="b0255-106">Il cmdlet **Set-AzIntegrationAccountAgreement** modifica un contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0255-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="b0255-107">Questo cmdlet restituisce un oggetto che rappresenta il contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0255-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="b0255-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="b0255-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="b0255-109">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri di modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="b0255-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b0255-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="b0255-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b0255-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="b0255-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b0255-112">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b0255-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b0255-113">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="b0255-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b0255-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0255-114">EXAMPLES</span></span>

### <span data-ttu-id="b0255-115">Esempio 1: Aggiornare un contratto di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="b0255-115">Example 1: Update an integration account agreement</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="b0255-116">Questo comando aggiorna un contratto di account di integrazione nel gruppo di risorse Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="b0255-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="b0255-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b0255-117">Example 2</span></span>

<span data-ttu-id="b0255-118">Modifica un contratto di integrazione con l'account.</span><span class="sxs-lookup"><span data-stu-id="b0255-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="b0255-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="b0255-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="b0255-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0255-120">PARAMETERS</span></span>

### <span data-ttu-id="b0255-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="b0255-121">-AgreementContent</span></span>
<span data-ttu-id="b0255-122">Specifica il contenuto del contratto, in formato JSON (JavaScript Object Notation), per il contratto.</span><span class="sxs-lookup"><span data-stu-id="b0255-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="b0255-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="b0255-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="b0255-124">Specifica il percorso del file del contenuto del contratto.</span><span class="sxs-lookup"><span data-stu-id="b0255-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="b0255-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="b0255-125">-AgreementName</span></span>
<span data-ttu-id="b0255-126">Specifica il nome del contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0255-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="b0255-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="b0255-127">-AgreementType</span></span>
<span data-ttu-id="b0255-128">Specifica il tipo di contratto dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0255-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="b0255-129">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b0255-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b0255-130">X12</span><span class="sxs-lookup"><span data-stu-id="b0255-130">X12</span></span> 
- <span data-ttu-id="b0255-131">AS2</span><span class="sxs-lookup"><span data-stu-id="b0255-131">AS2</span></span>
- <span data-ttu-id="b0255-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="b0255-132">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0255-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0255-133">-DefaultProfile</span></span>
<span data-ttu-id="b0255-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b0255-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0255-135">-Force</span><span class="sxs-lookup"><span data-stu-id="b0255-135">-Force</span></span>
<span data-ttu-id="b0255-136">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b0255-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0255-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="b0255-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="b0255-138">Specifica un qualificatore di identità aziendale del nome per il partner guest.</span><span class="sxs-lookup"><span data-stu-id="b0255-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="b0255-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="b0255-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="b0255-140">Valore qualificatore di qualificatore di identità guest per il contratto dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0255-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="b0255-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="b0255-141">-GuestPartner</span></span>
<span data-ttu-id="b0255-142">Specifica il nome del partner guest.</span><span class="sxs-lookup"><span data-stu-id="b0255-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="b0255-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="b0255-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="b0255-144">Specifica un qualificatore di identità business del nome per il partner host.</span><span class="sxs-lookup"><span data-stu-id="b0255-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="b0255-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="b0255-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="b0255-146">Valore qualificatore di identità host per il contratto dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0255-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="b0255-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="b0255-147">-HostPartner</span></span>
<span data-ttu-id="b0255-148">Specifica il nome del partner host.</span><span class="sxs-lookup"><span data-stu-id="b0255-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="b0255-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b0255-149">-Metadata</span></span>
<span data-ttu-id="b0255-150">Specifica un oggetto metadati per il contratto.</span><span class="sxs-lookup"><span data-stu-id="b0255-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="b0255-151">-Name</span><span class="sxs-lookup"><span data-stu-id="b0255-151">-Name</span></span>
<span data-ttu-id="b0255-152">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0255-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b0255-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0255-153">-ResourceGroupName</span></span>
<span data-ttu-id="b0255-154">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0255-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b0255-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0255-155">-Confirm</span></span>
<span data-ttu-id="b0255-156">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0255-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0255-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0255-157">-WhatIf</span></span>
<span data-ttu-id="b0255-158">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0255-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0255-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0255-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0255-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0255-160">CommonParameters</span></span>
<span data-ttu-id="b0255-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0255-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0255-162">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0255-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0255-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0255-163">INPUTS</span></span>

### <span data-ttu-id="b0255-164">System.String</span><span class="sxs-lookup"><span data-stu-id="b0255-164">System.String</span></span>

## <span data-ttu-id="b0255-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0255-165">OUTPUTS</span></span>

### <span data-ttu-id="b0255-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b0255-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="b0255-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0255-167">NOTES</span></span>

## <span data-ttu-id="b0255-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0255-168">RELATED LINKS</span></span>

[<span data-ttu-id="b0255-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b0255-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="b0255-170">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b0255-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="b0255-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b0255-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


