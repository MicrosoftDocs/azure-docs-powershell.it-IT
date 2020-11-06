---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 63241b764576e06166e293f17717b26c4dcbe3d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519578"
---
# <span data-ttu-id="5d112-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5d112-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="5d112-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d112-102">SYNOPSIS</span></span>
<span data-ttu-id="5d112-103">Rimuove un contratto per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5d112-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d112-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d112-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d112-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d112-105">DESCRIPTION</span></span>
<span data-ttu-id="5d112-106">Il cmdlet **Remove-AzureRmIntegrationAccountAgreement** rimuove un contratto di integrazione di un account da un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="5d112-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="5d112-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="5d112-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="5d112-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="5d112-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5d112-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="5d112-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5d112-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="5d112-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5d112-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="5d112-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5d112-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d112-112">EXAMPLES</span></span>

### <span data-ttu-id="5d112-113">Esempio 1: rimuovere un contratto di integrazione per nome</span><span class="sxs-lookup"><span data-stu-id="5d112-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="5d112-114">Questo comando rimuove il contratto per l'account di integrazione denominato IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="5d112-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="5d112-115">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="5d112-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5d112-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d112-116">PARAMETERS</span></span>

### <span data-ttu-id="5d112-117">-Contratto</span><span class="sxs-lookup"><span data-stu-id="5d112-117">-AgreementName</span></span>
<span data-ttu-id="5d112-118">Specifica il nome del contratto di integrazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="5d112-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="5d112-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5d112-119">-Force</span></span>
<span data-ttu-id="5d112-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5d112-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d112-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d112-121">-Name</span></span>
<span data-ttu-id="5d112-122">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5d112-122">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d112-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d112-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d112-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d112-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5d112-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5d112-125">-Confirm</span></span>
<span data-ttu-id="5d112-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d112-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d112-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d112-127">-WhatIf</span></span>
<span data-ttu-id="5d112-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d112-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d112-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d112-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d112-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d112-130">-DefaultProfile</span></span>
<span data-ttu-id="5d112-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d112-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d112-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d112-132">CommonParameters</span></span>
<span data-ttu-id="5d112-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d112-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d112-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d112-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d112-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d112-135">INPUTS</span></span>

## <span data-ttu-id="5d112-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d112-136">OUTPUTS</span></span>

## <span data-ttu-id="5d112-137">Note</span><span class="sxs-lookup"><span data-stu-id="5d112-137">NOTES</span></span>

## <span data-ttu-id="5d112-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d112-138">RELATED LINKS</span></span>

[<span data-ttu-id="5d112-139">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5d112-139">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="5d112-140">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5d112-140">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="5d112-141">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5d112-141">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


