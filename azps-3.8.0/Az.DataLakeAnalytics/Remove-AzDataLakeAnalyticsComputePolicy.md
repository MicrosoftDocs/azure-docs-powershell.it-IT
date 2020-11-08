---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018785"
---
# <span data-ttu-id="3c48f-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3c48f-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3c48f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c48f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c48f-103">Rimuove un criterio di calcolo di analisi dei dati di Azure Data Lake specificato</span><span class="sxs-lookup"><span data-stu-id="3c48f-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="3c48f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c48f-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c48f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c48f-105">DESCRIPTION</span></span>
<span data-ttu-id="3c48f-106">**Remove-AzDataLakeAnalyticsComputePolicy** rimuove un criterio di calcolo di analisi dei dati di Azure Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="3c48f-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="3c48f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c48f-107">EXAMPLES</span></span>

### <span data-ttu-id="3c48f-108">Esempio 1: rimuovere un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="3c48f-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="3c48f-109">Questo comando rimuove il criterio di calcolo specificato con il nome "criterio" nell'account "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="3c48f-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="3c48f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c48f-110">PARAMETERS</span></span>

### <span data-ttu-id="3c48f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3c48f-111">-Account</span></span>
<span data-ttu-id="3c48f-112">Nome dell'account da cui rimuovere i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="3c48f-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="3c48f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c48f-113">-DefaultProfile</span></span>
<span data-ttu-id="3c48f-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3c48f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c48f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c48f-115">-Name</span></span>
<span data-ttu-id="3c48f-116">Nome del criterio di calcolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3c48f-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="3c48f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c48f-117">-PassThru</span></span>
<span data-ttu-id="3c48f-118">Restituisce vero dopo l'eliminazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3c48f-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="3c48f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c48f-119">-ResourceGroupName</span></span>
<span data-ttu-id="3c48f-120">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="3c48f-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="3c48f-121">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3c48f-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="3c48f-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c48f-122">-Confirm</span></span>
<span data-ttu-id="3c48f-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c48f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c48f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c48f-124">-WhatIf</span></span>
<span data-ttu-id="3c48f-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c48f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c48f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c48f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c48f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c48f-127">CommonParameters</span></span>
<span data-ttu-id="3c48f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c48f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c48f-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c48f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c48f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c48f-130">INPUTS</span></span>

### <span data-ttu-id="3c48f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3c48f-131">System.String</span></span>

## <span data-ttu-id="3c48f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c48f-132">OUTPUTS</span></span>

### <span data-ttu-id="3c48f-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c48f-133">System.Boolean</span></span>

## <span data-ttu-id="3c48f-134">Note</span><span class="sxs-lookup"><span data-stu-id="3c48f-134">NOTES</span></span>

## <span data-ttu-id="3c48f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c48f-135">RELATED LINKS</span></span>
