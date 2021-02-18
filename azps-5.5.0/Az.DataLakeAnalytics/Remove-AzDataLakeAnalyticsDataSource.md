---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180926"
---
# <span data-ttu-id="28664-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="28664-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="28664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28664-102">SYNOPSIS</span></span>
<span data-ttu-id="28664-103">Rimuove un'origine dati da un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28664-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="28664-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28664-104">SYNTAX</span></span>

### <span data-ttu-id="28664-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28664-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28664-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28664-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28664-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28664-107">DESCRIPTION</span></span>
<span data-ttu-id="28664-108">Il cmdlet **Remove-AzDataLakeAnalyticsDataSource** rimuove un'origine dati da un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28664-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="28664-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28664-109">EXAMPLES</span></span>

### <span data-ttu-id="28664-110">Esempio 1: Rimuovere un'origine dati</span><span class="sxs-lookup"><span data-stu-id="28664-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="28664-111">Questo comando rimuove l'origine dati denominata AzureStorage01 dall'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="28664-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="28664-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28664-112">PARAMETERS</span></span>

### <span data-ttu-id="28664-113">-Account</span><span class="sxs-lookup"><span data-stu-id="28664-113">-Account</span></span>
<span data-ttu-id="28664-114">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28664-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="28664-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="28664-115">-Blob</span></span>
<span data-ttu-id="28664-116">Specifica il nome dell'account di archiviazione AzureBlob da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="28664-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28664-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28664-117">-DataLakeStore</span></span>
<span data-ttu-id="28664-118">Specifica il nome dell'account AzureData Lake Store da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="28664-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28664-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28664-119">-DefaultProfile</span></span>
<span data-ttu-id="28664-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="28664-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28664-121">-Force</span><span class="sxs-lookup"><span data-stu-id="28664-121">-Force</span></span>
<span data-ttu-id="28664-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="28664-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28664-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28664-123">-PassThru</span></span>
<span data-ttu-id="28664-124">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="28664-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28664-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="28664-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28664-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28664-126">-ResourceGroupName</span></span>
<span data-ttu-id="28664-127">Specifica il nome del gruppo di risorse dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="28664-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28664-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28664-128">-Confirm</span></span>
<span data-ttu-id="28664-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28664-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28664-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28664-130">-WhatIf</span></span>
<span data-ttu-id="28664-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28664-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28664-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28664-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28664-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28664-133">CommonParameters</span></span>
<span data-ttu-id="28664-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28664-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28664-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28664-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28664-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="28664-136">INPUTS</span></span>

### <span data-ttu-id="28664-137">System.String</span><span class="sxs-lookup"><span data-stu-id="28664-137">System.String</span></span>

## <span data-ttu-id="28664-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28664-138">OUTPUTS</span></span>

### <span data-ttu-id="28664-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28664-139">System.Boolean</span></span>

## <span data-ttu-id="28664-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="28664-140">NOTES</span></span>

## <span data-ttu-id="28664-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28664-141">RELATED LINKS</span></span>

[<span data-ttu-id="28664-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="28664-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="28664-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="28664-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


