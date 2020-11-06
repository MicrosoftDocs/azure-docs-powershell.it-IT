---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520118"
---
# <span data-ttu-id="dd065-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="dd065-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="dd065-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd065-102">SYNOPSIS</span></span>
<span data-ttu-id="dd065-103">Rimuove un criterio di calcolo di analisi dei dati di Azure Data Lake specificato</span><span class="sxs-lookup"><span data-stu-id="dd065-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd065-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd065-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd065-105">DESCRIPTION</span></span>
<span data-ttu-id="dd065-106">**Remove-AzureRmDataLakeAnalyticsComputePolicy** rimuove un criterio di calcolo di analisi dei dati di Azure Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="dd065-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="dd065-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd065-107">EXAMPLES</span></span>

### <span data-ttu-id="dd065-108">Esempio 1: rimuovere un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="dd065-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="dd065-109">Questo comando rimuove il criterio di calcolo specificato con il nome "criterio" nell'account "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="dd065-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="dd065-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd065-110">PARAMETERS</span></span>

### <span data-ttu-id="dd065-111">-Account</span><span class="sxs-lookup"><span data-stu-id="dd065-111">-Account</span></span>
<span data-ttu-id="dd065-112">Nome dell'account da cui rimuovere i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="dd065-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd065-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd065-113">-Name</span></span>
<span data-ttu-id="dd065-114">Nome del criterio di calcolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dd065-114">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd065-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd065-115">-PassThru</span></span>
<span data-ttu-id="dd065-116">Restituisce vero dopo l'eliminazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="dd065-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="dd065-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd065-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd065-118">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="dd065-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="dd065-119">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="dd065-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="dd065-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd065-120">-Confirm</span></span>
<span data-ttu-id="dd065-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd065-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd065-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd065-122">-WhatIf</span></span>
<span data-ttu-id="dd065-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd065-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd065-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd065-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd065-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd065-125">-DefaultProfile</span></span>
<span data-ttu-id="dd065-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd065-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd065-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd065-127">CommonParameters</span></span>
<span data-ttu-id="dd065-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd065-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd065-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd065-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd065-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd065-130">INPUTS</span></span>

### <span data-ttu-id="dd065-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dd065-131">System.String</span></span>

## <span data-ttu-id="dd065-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd065-132">OUTPUTS</span></span>

### <span data-ttu-id="dd065-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd065-133">System.Boolean</span></span>

## <span data-ttu-id="dd065-134">Note</span><span class="sxs-lookup"><span data-stu-id="dd065-134">NOTES</span></span>

## <span data-ttu-id="dd065-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd065-135">RELATED LINKS</span></span>

