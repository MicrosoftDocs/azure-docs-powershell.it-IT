---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 29846c8bb5650a667bf565fec273cbf24c8cd394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004254"
---
# <span data-ttu-id="01d96-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="01d96-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="01d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d96-102">SYNOPSIS</span></span>
<span data-ttu-id="01d96-103">Elimina un account di Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01d96-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="01d96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01d96-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01d96-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01d96-105">DESCRIPTION</span></span>
<span data-ttu-id="01d96-106">Il cmdlet **Remove-AzDataLakeAnalyticsAccount** elimina definitivamente un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01d96-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="01d96-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01d96-107">EXAMPLES</span></span>

### <span data-ttu-id="01d96-108">Esempio 1: Rimuovere un account</span><span class="sxs-lookup"><span data-stu-id="01d96-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="01d96-109">Questo comando rimuove l'account di Data Lake Analytics specificato.</span><span class="sxs-lookup"><span data-stu-id="01d96-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="01d96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01d96-110">PARAMETERS</span></span>

### <span data-ttu-id="01d96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d96-111">-DefaultProfile</span></span>
<span data-ttu-id="01d96-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="01d96-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01d96-113">-Force</span><span class="sxs-lookup"><span data-stu-id="01d96-113">-Force</span></span>
<span data-ttu-id="01d96-114">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="01d96-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d96-115">-Name</span><span class="sxs-lookup"><span data-stu-id="01d96-115">-Name</span></span>
<span data-ttu-id="01d96-116">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01d96-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01d96-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01d96-117">-PassThru</span></span>
<span data-ttu-id="01d96-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="01d96-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01d96-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="01d96-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d96-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d96-120">-ResourceGroupName</span></span>
<span data-ttu-id="01d96-121">Specifica il nome del gruppo di risorse dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="01d96-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01d96-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01d96-122">-Confirm</span></span>
<span data-ttu-id="01d96-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d96-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d96-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d96-124">-WhatIf</span></span>
<span data-ttu-id="01d96-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01d96-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01d96-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01d96-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d96-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d96-127">CommonParameters</span></span>
<span data-ttu-id="01d96-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d96-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d96-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d96-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d96-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="01d96-130">INPUTS</span></span>

### <span data-ttu-id="01d96-131">System.String</span><span class="sxs-lookup"><span data-stu-id="01d96-131">System.String</span></span>

## <span data-ttu-id="01d96-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01d96-132">OUTPUTS</span></span>

### <span data-ttu-id="01d96-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01d96-133">System.Boolean</span></span>

## <span data-ttu-id="01d96-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="01d96-134">NOTES</span></span>

## <span data-ttu-id="01d96-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01d96-135">RELATED LINKS</span></span>

[<span data-ttu-id="01d96-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="01d96-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="01d96-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="01d96-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="01d96-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="01d96-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="01d96-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="01d96-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


