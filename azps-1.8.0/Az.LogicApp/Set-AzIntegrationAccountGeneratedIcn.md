---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4dea211f2a09823161c1c6551b1fa00ab018a855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835376"
---
# <span data-ttu-id="a4a18-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="a4a18-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="a4a18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4a18-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a18-103">Aggiorna il numero di controllo dell'interscambio generato dall'account di integrazione nel gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a18-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="a4a18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4a18-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4a18-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4a18-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a18-106">Il cmdlet Set-AzIntegrationAccountGeneratedIcn aggiorna un numero di controllo interscambio generato (ICN) esistente per l'account di integrazione e restituisce un oggetto che rappresenta il numero di controllo dell'interscambio generato dall'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a4a18-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="a4a18-107">Questo cmdlet consente di aggiornare un numero di controllo dell'interscambio generato dall'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a4a18-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="a4a18-108">È possibile aggiornare un numero di controllo interscambio generato dall'account di integrazione specificando il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="a4a18-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="a4a18-109">Con questo comando non è possibile creare un nuovo account di integrazione con il numero di controllo interscambio generato.</span><span class="sxs-lookup"><span data-stu-id="a4a18-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="a4a18-110">Per usare i parametri dinamici, è sufficiente digitarli nel comando oppure digitare un segno meno (-) per indicare il nome di un parametro e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a4a18-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a4a18-111">Se si dimentica un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="a4a18-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="a4a18-112">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="a4a18-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="a4a18-113">Fornisci il parametro "-AgreementType" per specificare se i numeri di controllo X12 o EDIFACT restituiscono</span><span class="sxs-lookup"><span data-stu-id="a4a18-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="a4a18-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4a18-114">EXAMPLES</span></span>

### <span data-ttu-id="a4a18-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4a18-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="a4a18-116">Questo comando ottiene il numero di controllo dell'interscambio X12 generato dall'account di integrazione per un contratto specifico di integrazione, aumenta il valore di 100 e quindi scrive di nuovo il valore aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a4a18-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="a4a18-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a4a18-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="a4a18-118">Questo comando ottiene il numero di controllo dell'interscambio EdifactIntegrationAccountAgreement generato dall'account di integrazione per un contratto specifico di integrazione, aumenta il valore di 100 e quindi scrive di nuovo il valore aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a4a18-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="a4a18-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4a18-119">PARAMETERS</span></span>

### <span data-ttu-id="a4a18-120">-Contratto</span><span class="sxs-lookup"><span data-stu-id="a4a18-120">-AgreementName</span></span>
<span data-ttu-id="a4a18-121">Nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="a4a18-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="a4a18-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="a4a18-122">-AgreementType</span></span>
<span data-ttu-id="a4a18-123">Tipo di contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a4a18-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="a4a18-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="a4a18-124">-ControlNumber</span></span>
<span data-ttu-id="a4a18-125">Nuovo valore del numero di controllo generato.</span><span class="sxs-lookup"><span data-stu-id="a4a18-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="a4a18-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a18-126">-DefaultProfile</span></span>
<span data-ttu-id="a4a18-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a4a18-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4a18-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4a18-128">-Name</span></span>
<span data-ttu-id="a4a18-129">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a4a18-129">The integration account name.</span></span>

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

### <span data-ttu-id="a4a18-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a18-130">-ResourceGroupName</span></span>
<span data-ttu-id="a4a18-131">Nome del gruppo risorse account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a4a18-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="a4a18-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4a18-132">-Confirm</span></span>
<span data-ttu-id="a4a18-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a18-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4a18-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4a18-134">-WhatIf</span></span>
<span data-ttu-id="a4a18-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4a18-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4a18-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4a18-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4a18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a18-137">CommonParameters</span></span>
<span data-ttu-id="a4a18-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a18-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a18-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a18-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4a18-140">INPUTS</span></span>

### <span data-ttu-id="a4a18-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a4a18-141">System.String</span></span>

## <span data-ttu-id="a4a18-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4a18-142">OUTPUTS</span></span>

### <span data-ttu-id="a4a18-143">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="a4a18-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="a4a18-144">Note</span><span class="sxs-lookup"><span data-stu-id="a4a18-144">NOTES</span></span>

## <span data-ttu-id="a4a18-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4a18-145">RELATED LINKS</span></span>

[<span data-ttu-id="a4a18-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="a4a18-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

