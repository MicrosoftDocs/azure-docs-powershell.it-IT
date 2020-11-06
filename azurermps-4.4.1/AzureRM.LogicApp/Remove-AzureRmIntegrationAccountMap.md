---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: a7104f33fd2e5b9428b062bd8ac359ccabb25520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520061"
---
# <span data-ttu-id="5d5af-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d5af-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="5d5af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d5af-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5af-103">Rimuove una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5d5af-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d5af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d5af-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d5af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d5af-105">DESCRIPTION</span></span>
<span data-ttu-id="5d5af-106">Il cmdlet **Remove-AzureRmIntegrationAccountMap** rimuove una mappa dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d5af-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="5d5af-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="5d5af-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="5d5af-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="5d5af-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5d5af-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="5d5af-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5d5af-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="5d5af-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5d5af-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="5d5af-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5d5af-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d5af-112">EXAMPLES</span></span>

### <span data-ttu-id="5d5af-113">Esempio 1: rimuovere una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="5d5af-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="5d5af-114">Questo comando rimuove la mappa dell'account di integrazione denominata IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="5d5af-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="5d5af-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d5af-115">PARAMETERS</span></span>

### <span data-ttu-id="5d5af-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5d5af-116">-Force</span></span>
<span data-ttu-id="5d5af-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5d5af-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d5af-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="5d5af-118">-MapName</span></span>
<span data-ttu-id="5d5af-119">Specifica il nome della mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5d5af-119">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="5d5af-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d5af-120">-Name</span></span>
<span data-ttu-id="5d5af-121">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5d5af-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="5d5af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5af-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d5af-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d5af-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5d5af-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5d5af-124">-Confirm</span></span>
<span data-ttu-id="5d5af-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d5af-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5af-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5af-126">-WhatIf</span></span>
<span data-ttu-id="5d5af-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d5af-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d5af-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d5af-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5af-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5af-129">-DefaultProfile</span></span>
<span data-ttu-id="5d5af-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5af-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d5af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5af-131">CommonParameters</span></span>
<span data-ttu-id="5d5af-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5af-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5af-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d5af-134">INPUTS</span></span>

## <span data-ttu-id="5d5af-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d5af-135">OUTPUTS</span></span>

## <span data-ttu-id="5d5af-136">Note</span><span class="sxs-lookup"><span data-stu-id="5d5af-136">NOTES</span></span>

## <span data-ttu-id="5d5af-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d5af-137">RELATED LINKS</span></span>

[<span data-ttu-id="5d5af-138">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d5af-138">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="5d5af-139">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d5af-139">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="5d5af-140">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5d5af-140">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


