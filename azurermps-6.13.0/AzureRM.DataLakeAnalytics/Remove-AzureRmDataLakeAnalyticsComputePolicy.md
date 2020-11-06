---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: a97c6835144cda227fc07645f087e393cda2b8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511748"
---
# <span data-ttu-id="c8316-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c8316-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c8316-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8316-102">SYNOPSIS</span></span>
<span data-ttu-id="c8316-103">Rimuove un criterio di calcolo di analisi dei dati di Azure Data Lake specificato</span><span class="sxs-lookup"><span data-stu-id="c8316-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8316-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8316-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8316-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8316-105">DESCRIPTION</span></span>
<span data-ttu-id="c8316-106">**Remove-AzureRmDataLakeAnalyticsComputePolicy** rimuove un criterio di calcolo di analisi dei dati di Azure Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="c8316-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="c8316-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8316-107">EXAMPLES</span></span>

### <span data-ttu-id="c8316-108">Esempio 1: rimuovere un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="c8316-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="c8316-109">Questo comando rimuove il criterio di calcolo specificato con il nome "criterio" nell'account "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="c8316-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="c8316-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8316-110">PARAMETERS</span></span>

### <span data-ttu-id="c8316-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c8316-111">-Account</span></span>
<span data-ttu-id="c8316-112">Nome dell'account da cui rimuovere i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="c8316-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="c8316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8316-113">-DefaultProfile</span></span>
<span data-ttu-id="c8316-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c8316-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8316-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8316-115">-Name</span></span>
<span data-ttu-id="c8316-116">Nome del criterio di calcolo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c8316-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="c8316-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8316-117">-PassThru</span></span>
<span data-ttu-id="c8316-118">Restituisce vero dopo l'eliminazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c8316-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="c8316-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8316-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8316-120">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="c8316-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="c8316-121">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="c8316-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="c8316-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8316-122">-Confirm</span></span>
<span data-ttu-id="c8316-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8316-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8316-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8316-124">-WhatIf</span></span>
<span data-ttu-id="c8316-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8316-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8316-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8316-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8316-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8316-127">CommonParameters</span></span>
<span data-ttu-id="c8316-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8316-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8316-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8316-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8316-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8316-130">INPUTS</span></span>

### <span data-ttu-id="c8316-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c8316-131">System.String</span></span>

## <span data-ttu-id="c8316-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8316-132">OUTPUTS</span></span>

### <span data-ttu-id="c8316-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8316-133">System.Boolean</span></span>

## <span data-ttu-id="c8316-134">Note</span><span class="sxs-lookup"><span data-stu-id="c8316-134">NOTES</span></span>

## <span data-ttu-id="c8316-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8316-135">RELATED LINKS</span></span>
