---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 43f1ac12e6f88faa43dcc4f96157425f2e180680
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684548"
---
# <span data-ttu-id="30ece-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="30ece-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="30ece-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30ece-102">SYNOPSIS</span></span>
<span data-ttu-id="30ece-103">Rimuove un'origine dati da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="30ece-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="30ece-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30ece-104">SYNTAX</span></span>

### <span data-ttu-id="30ece-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30ece-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30ece-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30ece-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30ece-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30ece-107">DESCRIPTION</span></span>
<span data-ttu-id="30ece-108">Il cmdlet **Remove-AzDataLakeAnalyticsDataSource** consente di rimuovere un'origine dati da un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="30ece-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="30ece-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30ece-109">EXAMPLES</span></span>

### <span data-ttu-id="30ece-110">Esempio 1: rimuovere un'origine dati</span><span class="sxs-lookup"><span data-stu-id="30ece-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="30ece-111">Questo comando rimuove l'origine dati denominata AzureStorage01 dall'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="30ece-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="30ece-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30ece-112">PARAMETERS</span></span>

### <span data-ttu-id="30ece-113">-Account</span><span class="sxs-lookup"><span data-stu-id="30ece-113">-Account</span></span>
<span data-ttu-id="30ece-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="30ece-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="30ece-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="30ece-115">-Blob</span></span>
<span data-ttu-id="30ece-116">Specifica il nome dell'account di archiviazione di AzureBlob da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="30ece-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="30ece-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30ece-117">-DataLakeStore</span></span>
<span data-ttu-id="30ece-118">Specifica il nome dell'account di AzureData Lake Store da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="30ece-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="30ece-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ece-119">-DefaultProfile</span></span>
<span data-ttu-id="30ece-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30ece-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30ece-121">-Force</span><span class="sxs-lookup"><span data-stu-id="30ece-121">-Force</span></span>
<span data-ttu-id="30ece-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="30ece-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30ece-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30ece-123">-PassThru</span></span>
<span data-ttu-id="30ece-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="30ece-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="30ece-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="30ece-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="30ece-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ece-126">-ResourceGroupName</span></span>
<span data-ttu-id="30ece-127">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="30ece-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="30ece-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30ece-128">-Confirm</span></span>
<span data-ttu-id="30ece-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30ece-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30ece-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ece-130">-WhatIf</span></span>
<span data-ttu-id="30ece-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30ece-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30ece-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30ece-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30ece-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ece-133">CommonParameters</span></span>
<span data-ttu-id="30ece-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ece-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ece-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ece-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ece-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30ece-136">INPUTS</span></span>

### <span data-ttu-id="30ece-137">System. String</span><span class="sxs-lookup"><span data-stu-id="30ece-137">System.String</span></span>

## <span data-ttu-id="30ece-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30ece-138">OUTPUTS</span></span>

### <span data-ttu-id="30ece-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30ece-139">System.Boolean</span></span>

## <span data-ttu-id="30ece-140">Note</span><span class="sxs-lookup"><span data-stu-id="30ece-140">NOTES</span></span>

## <span data-ttu-id="30ece-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30ece-141">RELATED LINKS</span></span>

[<span data-ttu-id="30ece-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="30ece-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="30ece-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="30ece-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)

