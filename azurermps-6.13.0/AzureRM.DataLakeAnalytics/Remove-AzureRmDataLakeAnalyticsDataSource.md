---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 43f9c55e6da93392e95191d1b601f771221e1caa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686428"
---
# <span data-ttu-id="33a28-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="33a28-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="33a28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33a28-102">SYNOPSIS</span></span>
<span data-ttu-id="33a28-103">Rimuove un'origine dati da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="33a28-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33a28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33a28-104">SYNTAX</span></span>

### <span data-ttu-id="33a28-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33a28-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33a28-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33a28-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33a28-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33a28-107">DESCRIPTION</span></span>
<span data-ttu-id="33a28-108">Il cmdlet **Remove-AzureRmDataLakeAnalyticsDataSource** consente di rimuovere un'origine dati da un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="33a28-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="33a28-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33a28-109">EXAMPLES</span></span>

### <span data-ttu-id="33a28-110">Esempio 1: rimuovere un'origine dati</span><span class="sxs-lookup"><span data-stu-id="33a28-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="33a28-111">Questo comando rimuove l'origine dati denominata AzureStorage01 dall'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="33a28-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="33a28-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33a28-112">PARAMETERS</span></span>

### <span data-ttu-id="33a28-113">-Account</span><span class="sxs-lookup"><span data-stu-id="33a28-113">-Account</span></span>
<span data-ttu-id="33a28-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="33a28-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="33a28-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="33a28-115">-Blob</span></span>
<span data-ttu-id="33a28-116">Specifica il nome dell'account di archiviazione di AzureBlob da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="33a28-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="33a28-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33a28-117">-DataLakeStore</span></span>
<span data-ttu-id="33a28-118">Specifica il nome dell'account di AzureData Lake Store da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="33a28-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="33a28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a28-119">-DefaultProfile</span></span>
<span data-ttu-id="33a28-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="33a28-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33a28-121">-Force</span><span class="sxs-lookup"><span data-stu-id="33a28-121">-Force</span></span>
<span data-ttu-id="33a28-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="33a28-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="33a28-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33a28-123">-PassThru</span></span>
<span data-ttu-id="33a28-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="33a28-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33a28-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="33a28-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33a28-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a28-126">-ResourceGroupName</span></span>
<span data-ttu-id="33a28-127">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="33a28-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="33a28-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="33a28-128">-Confirm</span></span>
<span data-ttu-id="33a28-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a28-130">-WhatIf</span></span>
<span data-ttu-id="33a28-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33a28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a28-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33a28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a28-133">CommonParameters</span></span>
<span data-ttu-id="33a28-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a28-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a28-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a28-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33a28-136">INPUTS</span></span>

### <span data-ttu-id="33a28-137">System. String</span><span class="sxs-lookup"><span data-stu-id="33a28-137">System.String</span></span>

## <span data-ttu-id="33a28-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33a28-138">OUTPUTS</span></span>

### <span data-ttu-id="33a28-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33a28-139">System.Boolean</span></span>

## <span data-ttu-id="33a28-140">Note</span><span class="sxs-lookup"><span data-stu-id="33a28-140">NOTES</span></span>

## <span data-ttu-id="33a28-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33a28-141">RELATED LINKS</span></span>

[<span data-ttu-id="33a28-142">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="33a28-142">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="33a28-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="33a28-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


