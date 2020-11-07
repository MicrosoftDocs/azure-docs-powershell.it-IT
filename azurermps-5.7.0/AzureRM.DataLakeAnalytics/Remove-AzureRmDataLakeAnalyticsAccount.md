---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: f978925766fb664f5ddeaf3b6dffa94e55244f43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685837"
---
# <span data-ttu-id="8a40d-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8a40d-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="8a40d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a40d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a40d-103">Elimina un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="8a40d-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a40d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a40d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a40d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a40d-105">DESCRIPTION</span></span>
<span data-ttu-id="8a40d-106">Il cmdlet **Remove-AzureRmDataLakeAnalyticsAccount** Elimina definitivamente un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="8a40d-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8a40d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a40d-107">EXAMPLES</span></span>

### <span data-ttu-id="8a40d-108">Esempio 1: rimuovere un account</span><span class="sxs-lookup"><span data-stu-id="8a40d-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="8a40d-109">Questo comando rimuove l'account di analisi dei dati del lago specificato.</span><span class="sxs-lookup"><span data-stu-id="8a40d-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="8a40d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a40d-110">PARAMETERS</span></span>

### <span data-ttu-id="8a40d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a40d-111">-DefaultProfile</span></span>
<span data-ttu-id="8a40d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8a40d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a40d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8a40d-113">-Force</span></span>
<span data-ttu-id="8a40d-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8a40d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a40d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a40d-115">-Name</span></span>
<span data-ttu-id="8a40d-116">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="8a40d-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a40d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a40d-117">-PassThru</span></span>
<span data-ttu-id="8a40d-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8a40d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a40d-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8a40d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8a40d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a40d-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a40d-121">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="8a40d-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a40d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a40d-122">-Confirm</span></span>
<span data-ttu-id="8a40d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a40d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a40d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a40d-124">-WhatIf</span></span>
<span data-ttu-id="8a40d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a40d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a40d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a40d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a40d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a40d-127">CommonParameters</span></span>
<span data-ttu-id="8a40d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a40d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a40d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a40d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a40d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a40d-130">INPUTS</span></span>

### <span data-ttu-id="8a40d-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a40d-131">None</span></span>
<span data-ttu-id="8a40d-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8a40d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a40d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a40d-133">OUTPUTS</span></span>

### <span data-ttu-id="8a40d-134">bool</span><span class="sxs-lookup"><span data-stu-id="8a40d-134">bool</span></span>
<span data-ttu-id="8a40d-135">Se PassThru è specificato, restituisce vero al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8a40d-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="8a40d-136">Note</span><span class="sxs-lookup"><span data-stu-id="8a40d-136">NOTES</span></span>

## <span data-ttu-id="8a40d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a40d-137">RELATED LINKS</span></span>

[<span data-ttu-id="8a40d-138">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8a40d-138">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8a40d-139">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8a40d-139">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8a40d-140">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8a40d-140">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="8a40d-141">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="8a40d-141">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


