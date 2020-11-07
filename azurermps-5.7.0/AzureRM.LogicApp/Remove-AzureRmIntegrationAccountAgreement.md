---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 88661e132e6f40f4bb8e90fac339ddf1946085c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686314"
---
# <span data-ttu-id="33328-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="33328-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="33328-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33328-102">SYNOPSIS</span></span>
<span data-ttu-id="33328-103">Rimuove un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="33328-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33328-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33328-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33328-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33328-105">DESCRIPTION</span></span>
<span data-ttu-id="33328-106">Il cmdlet **Remove-AzureRmIntegrationAccountAgreement** rimuove un contratto di integrazione di un account da un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="33328-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="33328-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="33328-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="33328-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="33328-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="33328-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="33328-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="33328-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="33328-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="33328-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="33328-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="33328-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33328-112">EXAMPLES</span></span>

### <span data-ttu-id="33328-113">Esempio 1: rimuovere un contratto di integrazione per nome</span><span class="sxs-lookup"><span data-stu-id="33328-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="33328-114">Questo comando rimuove il contratto per l'account di integrazione denominato IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="33328-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="33328-115">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="33328-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="33328-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33328-116">PARAMETERS</span></span>

### <span data-ttu-id="33328-117">-Contratto</span><span class="sxs-lookup"><span data-stu-id="33328-117">-AgreementName</span></span>
<span data-ttu-id="33328-118">Specifica il nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="33328-118">Specifies the name of the integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33328-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33328-119">-DefaultProfile</span></span>
<span data-ttu-id="33328-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="33328-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33328-121">-Force</span><span class="sxs-lookup"><span data-stu-id="33328-121">-Force</span></span>
<span data-ttu-id="33328-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="33328-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="33328-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="33328-123">-Name</span></span>
<span data-ttu-id="33328-124">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="33328-124">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33328-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33328-125">-ResourceGroupName</span></span>
<span data-ttu-id="33328-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33328-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="33328-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="33328-127">-Confirm</span></span>
<span data-ttu-id="33328-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33328-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33328-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33328-129">-WhatIf</span></span>
<span data-ttu-id="33328-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33328-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33328-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33328-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33328-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33328-132">CommonParameters</span></span>
<span data-ttu-id="33328-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33328-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33328-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33328-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33328-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33328-135">INPUTS</span></span>

### <span data-ttu-id="33328-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="33328-136">None</span></span>
<span data-ttu-id="33328-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="33328-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33328-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33328-138">OUTPUTS</span></span>

## <span data-ttu-id="33328-139">Note</span><span class="sxs-lookup"><span data-stu-id="33328-139">NOTES</span></span>

## <span data-ttu-id="33328-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33328-140">RELATED LINKS</span></span>

[<span data-ttu-id="33328-141">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="33328-141">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="33328-142">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="33328-142">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="33328-143">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="33328-143">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


