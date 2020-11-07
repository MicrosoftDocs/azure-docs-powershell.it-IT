---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 79ad0434a7918bbdf834b5917ed023cbbabf0525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685982"
---
# <span data-ttu-id="f1fb0-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f1fb0-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="f1fb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fb0-103">Modifica un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1fb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1fb0-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1fb0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1fb0-105">DESCRIPTION</span></span>
<span data-ttu-id="f1fb0-106">Il cmdlet **set-AzureRmIntegrationAccountAgreement** modifica un contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="f1fb0-107">Questo cmdlet restituisce un oggetto che rappresenta il contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="f1fb0-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-108">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="f1fb0-109">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="f1fb0-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f1fb0-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f1fb0-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f1fb0-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f1fb0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1fb0-114">EXAMPLES</span></span>

### <span data-ttu-id="f1fb0-115">Esempio 1: aggiornare un contratto per l'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="f1fb0-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="f1fb0-116">Questo comando aggiorna un contratto per l'account di integrazione nel gruppo di risorse Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="f1fb0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1fb0-117">PARAMETERS</span></span>

### <span data-ttu-id="f1fb0-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="f1fb0-118">-AgreementContent</span></span>
<span data-ttu-id="f1fb0-119">Specifica il contenuto del contratto, in formato JSON (JavaScript Object Notation) per il contratto.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="f1fb0-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="f1fb0-121">Specifica il percorso del file del contenuto del contratto per il contratto.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-121">Specifies the file path of agreement content for the agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-122">-Contratto</span><span class="sxs-lookup"><span data-stu-id="f1fb0-122">-AgreementName</span></span>
<span data-ttu-id="f1fb0-123">Specifica il nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-123">Specifies the name of the integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="f1fb0-124">-AgreementType</span></span>
<span data-ttu-id="f1fb0-125">Specifica il tipo di contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="f1fb0-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1fb0-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1fb0-127">X12</span><span class="sxs-lookup"><span data-stu-id="f1fb0-127">X12</span></span> 
- <span data-ttu-id="f1fb0-128">AS2</span><span class="sxs-lookup"><span data-stu-id="f1fb0-128">AS2</span></span>
- <span data-ttu-id="f1fb0-129">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="f1fb0-129">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fb0-130">-DefaultProfile</span></span>
<span data-ttu-id="f1fb0-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f1fb0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f1fb0-132">-Force</span></span>
<span data-ttu-id="f1fb0-133">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="f1fb0-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="f1fb0-135">Specifica un qualificatore di identità aziendale per il partner guest.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-135">Specifies a name business identity qualifier for the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="f1fb0-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="f1fb0-137">Il valore del qualificatore dell'identità Guest Integration Agreement.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-137">The integration account agreement guest identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="f1fb0-138">-GuestPartner</span></span>
<span data-ttu-id="f1fb0-139">Specifica il nome del partner guest.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-139">Specifies the name of the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="f1fb0-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="f1fb0-141">Specifica un qualificatore di identità aziendale per il partner host.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-141">Specifies a name business identity qualifier for the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="f1fb0-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="f1fb0-143">Valore del qualificatore dell'identità host del contratto di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-143">The integration account agreement host identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-144">-Capofila Segds</span><span class="sxs-lookup"><span data-stu-id="f1fb0-144">-HostPartner</span></span>
<span data-ttu-id="f1fb0-145">Specifica il nome del partner host.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-145">Specifies the name of the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f1fb0-146">-Metadata</span></span>
<span data-ttu-id="f1fb0-147">Specifica un oggetto Metadata per il contratto.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1fb0-148">-Name</span></span>
<span data-ttu-id="f1fb0-149">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-149">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1fb0-150">-ResourceGroupName</span></span>
<span data-ttu-id="f1fb0-151">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-151">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f1fb0-152">-Confirm</span></span>
<span data-ttu-id="f1fb0-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1fb0-154">-WhatIf</span></span>
<span data-ttu-id="f1fb0-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1fb0-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1fb0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fb0-157">CommonParameters</span></span>
<span data-ttu-id="f1fb0-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fb0-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1fb0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fb0-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1fb0-160">INPUTS</span></span>

### <span data-ttu-id="f1fb0-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f1fb0-161">None</span></span>
<span data-ttu-id="f1fb0-162">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f1fb0-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1fb0-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1fb0-163">OUTPUTS</span></span>

### <span data-ttu-id="f1fb0-164">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f1fb0-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="f1fb0-165">Note</span><span class="sxs-lookup"><span data-stu-id="f1fb0-165">NOTES</span></span>

## <span data-ttu-id="f1fb0-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1fb0-166">RELATED LINKS</span></span>

[<span data-ttu-id="f1fb0-167">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f1fb0-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f1fb0-168">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f1fb0-168">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f1fb0-169">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f1fb0-169">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

