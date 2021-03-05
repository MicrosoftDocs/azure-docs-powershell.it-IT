---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1e6f6957adc8a67e1d92c0aad6f2be035b4f390d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963118"
---
# <span data-ttu-id="fdb5e-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fdb5e-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fdb5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb5e-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb5e-103">Rimuove un criterio di elaborazione di Azure Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="fdb5e-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="fdb5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdb5e-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb5e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fdb5e-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb5e-106">**Remove-AzDataLakeAnalyticsComputePolicy** rimuove un criterio di calcolo di Azure Data Lake Analytics specificato.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="fdb5e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdb5e-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb5e-108">Esempio 1: Rimuovere un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="fdb5e-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="fdb5e-109">Questo comando rimuove il criterio di elaborazione specificato con il nome 'myPolicy' nell'account 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="fdb5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdb5e-110">PARAMETERS</span></span>

### <span data-ttu-id="fdb5e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="fdb5e-111">-Account</span></span>
<span data-ttu-id="fdb5e-112">Nome dell'account da cui rimuovere il criterio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="fdb5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb5e-113">-DefaultProfile</span></span>
<span data-ttu-id="fdb5e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fdb5e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdb5e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fdb5e-115">-Name</span></span>
<span data-ttu-id="fdb5e-116">Nome del criterio di calcolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="fdb5e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdb5e-117">-PassThru</span></span>
<span data-ttu-id="fdb5e-118">Restituisce true dopo l'eliminazione corretta.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="fdb5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="fdb5e-120">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="fdb5e-121">Facoltativo e tenterà di individuarne uno, se non specificato.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="fdb5e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdb5e-122">-Confirm</span></span>
<span data-ttu-id="fdb5e-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb5e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb5e-124">-WhatIf</span></span>
<span data-ttu-id="fdb5e-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb5e-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb5e-127">CommonParameters</span></span>
<span data-ttu-id="fdb5e-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb5e-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb5e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb5e-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="fdb5e-130">INPUTS</span></span>

### <span data-ttu-id="fdb5e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fdb5e-131">System.String</span></span>

## <span data-ttu-id="fdb5e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdb5e-132">OUTPUTS</span></span>

### <span data-ttu-id="fdb5e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fdb5e-133">System.Boolean</span></span>

## <span data-ttu-id="fdb5e-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="fdb5e-134">NOTES</span></span>

## <span data-ttu-id="fdb5e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdb5e-135">RELATED LINKS</span></span>
