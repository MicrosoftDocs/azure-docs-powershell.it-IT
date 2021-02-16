---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187567"
---
# <span data-ttu-id="68c29-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="68c29-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="68c29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68c29-102">SYNOPSIS</span></span>
<span data-ttu-id="68c29-103">Aggiorna il numero di controllo interscambio generato dall'account di integrazione nel gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="68c29-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="68c29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68c29-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c29-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="68c29-105">DESCRIPTION</span></span>
<span data-ttu-id="68c29-106">Il cmdlet Set-AzIntegrationAccountGeneratedIcn aggiorna un numero di controllo interscambio generato da un account di integrazione esistente e restituisce un oggetto che rappresenta il numero di controllo interscambio generato dall'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="68c29-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="68c29-107">Usare questo cmdlet per aggiornare un numero di controllo interscambio generato da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="68c29-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="68c29-108">È possibile aggiornare un numero di controllo interscambio generato da un account di integrazione specificando il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="68c29-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="68c29-109">Con questo comando non è possibile creare un nuovo numero di controllo di interscambio generato da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="68c29-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="68c29-110">Per usare i parametri dinamici, è sufficiente digitarli nel comando oppure digitare un segno meno (-) per indicare il nome di un parametro e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="68c29-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="68c29-111">Se non si specifica un parametro del modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="68c29-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="68c29-112">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri di modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="68c29-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="68c29-113">Specifica il parametro "-AgreementType" per specificare se i numeri di controllo X12 o Edifact devono restituire</span><span class="sxs-lookup"><span data-stu-id="68c29-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="68c29-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68c29-114">EXAMPLES</span></span>

### <span data-ttu-id="68c29-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68c29-115">Example 1</span></span>
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

<span data-ttu-id="68c29-116">Questo comando recupera il numero di controllo interscambio X12 generato dall'account di integrazione per uno specifico contratto di account di integrazione, ne aumenta il valore di 100 e quindi scrive di nuovo il valore aggiornato.</span><span class="sxs-lookup"><span data-stu-id="68c29-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="68c29-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="68c29-117">Example 2</span></span>
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

<span data-ttu-id="68c29-118">Questo comando recupera il numero di controllo interscambio edifactIntegrationAccountAgreement generato dall'account di integrazione per uno specifico contratto di account di integrazione, ne aumenta il valore di 100 e quindi scrive di nuovo il valore aggiornato.</span><span class="sxs-lookup"><span data-stu-id="68c29-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="68c29-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68c29-119">PARAMETERS</span></span>

### <span data-ttu-id="68c29-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="68c29-120">-AgreementName</span></span>
<span data-ttu-id="68c29-121">Nome del contratto di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="68c29-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="68c29-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="68c29-122">-AgreementType</span></span>
<span data-ttu-id="68c29-123">Tipo di contratto dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="68c29-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="68c29-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="68c29-124">-ControlNumber</span></span>
<span data-ttu-id="68c29-125">Nuovo valore del numero di controllo generato.</span><span class="sxs-lookup"><span data-stu-id="68c29-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="68c29-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c29-126">-DefaultProfile</span></span>
<span data-ttu-id="68c29-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="68c29-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68c29-128">-Name</span><span class="sxs-lookup"><span data-stu-id="68c29-128">-Name</span></span>
<span data-ttu-id="68c29-129">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="68c29-129">The integration account name.</span></span>

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

### <span data-ttu-id="68c29-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68c29-130">-ResourceGroupName</span></span>
<span data-ttu-id="68c29-131">Nome del gruppo di risorse dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="68c29-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="68c29-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68c29-132">-Confirm</span></span>
<span data-ttu-id="68c29-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c29-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68c29-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c29-134">-WhatIf</span></span>
<span data-ttu-id="68c29-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68c29-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68c29-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68c29-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68c29-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c29-137">CommonParameters</span></span>
<span data-ttu-id="68c29-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68c29-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c29-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68c29-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c29-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="68c29-140">INPUTS</span></span>

### <span data-ttu-id="68c29-141">System.String</span><span class="sxs-lookup"><span data-stu-id="68c29-141">System.String</span></span>

## <span data-ttu-id="68c29-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68c29-142">OUTPUTS</span></span>

### <span data-ttu-id="68c29-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="68c29-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="68c29-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="68c29-144">NOTES</span></span>

## <span data-ttu-id="68c29-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68c29-145">RELATED LINKS</span></span>

[<span data-ttu-id="68c29-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="68c29-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

