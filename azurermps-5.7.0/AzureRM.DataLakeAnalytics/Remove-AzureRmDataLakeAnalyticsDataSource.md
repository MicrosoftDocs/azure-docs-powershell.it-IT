---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2707100452f9b64c093b4ae52c724e09f6cfe6e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514407"
---
# <span data-ttu-id="ccdda-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ccdda-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="ccdda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccdda-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdda-103">Rimuove un'origine dati da un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="ccdda-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccdda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccdda-104">SYNTAX</span></span>

### <span data-ttu-id="ccdda-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ccdda-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccdda-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ccdda-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccdda-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccdda-107">DESCRIPTION</span></span>
<span data-ttu-id="ccdda-108">Il cmdlet **Remove-AzureRmDataLakeAnalyticsDataSource** consente di rimuovere un'origine dati da un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ccdda-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ccdda-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccdda-109">EXAMPLES</span></span>

### <span data-ttu-id="ccdda-110">Esempio 1: rimuovere un'origine dati</span><span class="sxs-lookup"><span data-stu-id="ccdda-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="ccdda-111">Questo comando rimuove l'origine dati denominata AzureStorage01 dall'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="ccdda-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="ccdda-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccdda-112">PARAMETERS</span></span>

### <span data-ttu-id="ccdda-113">-Account</span><span class="sxs-lookup"><span data-stu-id="ccdda-113">-Account</span></span>
<span data-ttu-id="ccdda-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="ccdda-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ccdda-115">-Blob</span></span>
<span data-ttu-id="ccdda-116">Specifica il nome dell'account di archiviazione di AzureBlob da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ccdda-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ccdda-117">-DataLakeStore</span></span>
<span data-ttu-id="ccdda-118">Specifica il nome dell'account di AzureData Lake Store da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ccdda-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdda-119">-DefaultProfile</span></span>
<span data-ttu-id="ccdda-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ccdda-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ccdda-121">-Force</span></span>
<span data-ttu-id="ccdda-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ccdda-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccdda-123">-PassThru</span></span>
<span data-ttu-id="ccdda-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ccdda-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ccdda-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ccdda-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdda-126">-ResourceGroupName</span></span>
<span data-ttu-id="ccdda-127">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="ccdda-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ccdda-128">-Confirm</span></span>
<span data-ttu-id="ccdda-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccdda-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdda-130">-WhatIf</span></span>
<span data-ttu-id="ccdda-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccdda-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdda-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccdda-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdda-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdda-133">CommonParameters</span></span>
<span data-ttu-id="ccdda-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdda-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdda-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccdda-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdda-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccdda-136">INPUTS</span></span>

### <span data-ttu-id="ccdda-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ccdda-137">None</span></span>
<span data-ttu-id="ccdda-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ccdda-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ccdda-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccdda-139">OUTPUTS</span></span>

### <span data-ttu-id="ccdda-140">bool</span><span class="sxs-lookup"><span data-stu-id="ccdda-140">bool</span></span>
<span data-ttu-id="ccdda-141">Se PassThru è specificato, restituisce vero al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ccdda-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="ccdda-142">Note</span><span class="sxs-lookup"><span data-stu-id="ccdda-142">NOTES</span></span>

## <span data-ttu-id="ccdda-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccdda-143">RELATED LINKS</span></span>

[<span data-ttu-id="ccdda-144">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ccdda-144">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="ccdda-145">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ccdda-145">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


