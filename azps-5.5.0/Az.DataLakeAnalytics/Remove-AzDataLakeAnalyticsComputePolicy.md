---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194791"
---
# <span data-ttu-id="b089a-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b089a-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b089a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b089a-102">SYNOPSIS</span></span>
<span data-ttu-id="b089a-103">Rimuove un criterio di calcolo Azure Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="b089a-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="b089a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b089a-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b089a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b089a-105">DESCRIPTION</span></span>
<span data-ttu-id="b089a-106">**Remove-AzDataLakeAnalyticsComputePolicy** rimuove un criterio di calcolo di Azure Data Lake Analytics specificato.</span><span class="sxs-lookup"><span data-stu-id="b089a-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="b089a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b089a-107">EXAMPLES</span></span>

### <span data-ttu-id="b089a-108">Esempio 1: Rimuovere un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="b089a-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="b089a-109">Questo comando rimuove il criterio di elaborazione specificato con il nome 'myPolicy' nell'account 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="b089a-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="b089a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b089a-110">PARAMETERS</span></span>

### <span data-ttu-id="b089a-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b089a-111">-Account</span></span>
<span data-ttu-id="b089a-112">Nome dell'account da cui rimuovere i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="b089a-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="b089a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b089a-113">-DefaultProfile</span></span>
<span data-ttu-id="b089a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b089a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b089a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b089a-115">-Name</span></span>
<span data-ttu-id="b089a-116">Nome del criterio di calcolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b089a-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="b089a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b089a-117">-PassThru</span></span>
<span data-ttu-id="b089a-118">Restituisce true dopo l'eliminazione corretta.</span><span class="sxs-lookup"><span data-stu-id="b089a-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="b089a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b089a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b089a-120">Nome del gruppo di risorse in cui esiste l'account.</span><span class="sxs-lookup"><span data-stu-id="b089a-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="b089a-121">Facoltativo e tenterà di individuarne l'errore, se non specificato.</span><span class="sxs-lookup"><span data-stu-id="b089a-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="b089a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b089a-122">-Confirm</span></span>
<span data-ttu-id="b089a-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b089a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b089a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b089a-124">-WhatIf</span></span>
<span data-ttu-id="b089a-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b089a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b089a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b089a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b089a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b089a-127">CommonParameters</span></span>
<span data-ttu-id="b089a-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b089a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b089a-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b089a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b089a-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="b089a-130">INPUTS</span></span>

### <span data-ttu-id="b089a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b089a-131">System.String</span></span>

## <span data-ttu-id="b089a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b089a-132">OUTPUTS</span></span>

### <span data-ttu-id="b089a-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b089a-133">System.Boolean</span></span>

## <span data-ttu-id="b089a-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="b089a-134">NOTES</span></span>

## <span data-ttu-id="b089a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b089a-135">RELATED LINKS</span></span>
