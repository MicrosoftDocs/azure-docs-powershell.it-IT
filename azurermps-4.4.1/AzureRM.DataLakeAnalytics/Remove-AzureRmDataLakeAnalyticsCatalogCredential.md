---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: fc25b0a6605632da44d2b198c4bb30c515b2e456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510664"
---
# <span data-ttu-id="016b0-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="016b0-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="016b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="016b0-102">SYNOPSIS</span></span>
<span data-ttu-id="016b0-103">Elimina una credenziale di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="016b0-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="016b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="016b0-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="016b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="016b0-105">DESCRIPTION</span></span>
<span data-ttu-id="016b0-106">Il cmdlet Remove-AzureRmDataLakeAnalyticsCatalogCredential Elimina le credenziali di un catalogo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="016b0-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="016b0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="016b0-107">EXAMPLES</span></span>

### <span data-ttu-id="016b0-108">Esempio 1: rimuovere una credenziale</span><span class="sxs-lookup"><span data-stu-id="016b0-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="016b0-109">Questo comando consente di rimuovere le credenziali del catalogo dei dati del lago analitico specificato.</span><span class="sxs-lookup"><span data-stu-id="016b0-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="016b0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="016b0-110">PARAMETERS</span></span>

### <span data-ttu-id="016b0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="016b0-111">-Account</span></span>
<span data-ttu-id="016b0-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="016b0-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="016b0-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="016b0-113">-DatabaseName</span></span>
<span data-ttu-id="016b0-114">Specifica il nome del database che contiene le credenziali.</span><span class="sxs-lookup"><span data-stu-id="016b0-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="016b0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="016b0-115">-Force</span></span>
<span data-ttu-id="016b0-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="016b0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="016b0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="016b0-117">-Name</span></span>
<span data-ttu-id="016b0-118">Specifica il nome della credenziale.</span><span class="sxs-lookup"><span data-stu-id="016b0-118">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="016b0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="016b0-119">-PassThru</span></span>
<span data-ttu-id="016b0-120">Indica che il cmdlet non attende il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="016b0-120">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="016b0-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="016b0-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="016b0-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="016b0-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="016b0-123">-Password</span><span class="sxs-lookup"><span data-stu-id="016b0-123">-Password</span></span>
<span data-ttu-id="016b0-124">La password per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="016b0-124">The password for the credential.</span></span>
<span data-ttu-id="016b0-125">Questa operazione è obbligatoria se il chiamante non è il proprietario dell'account.</span><span class="sxs-lookup"><span data-stu-id="016b0-125">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="016b0-126">-Recurse</span><span class="sxs-lookup"><span data-stu-id="016b0-126">-Recurse</span></span>
<span data-ttu-id="016b0-127">Indica che questa operazione di eliminazione deve passare e anche eliminare e rilasciare tutte le risorse dipendenti da questa credenziale.</span><span class="sxs-lookup"><span data-stu-id="016b0-127">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="016b0-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="016b0-128">-Confirm</span></span>
<span data-ttu-id="016b0-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="016b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="016b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="016b0-130">-WhatIf</span></span>
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

### <span data-ttu-id="016b0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016b0-131">-DefaultProfile</span></span>
<span data-ttu-id="016b0-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="016b0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="016b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016b0-133">CommonParameters</span></span>
<span data-ttu-id="016b0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="016b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016b0-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="016b0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016b0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="016b0-136">INPUTS</span></span>

## <span data-ttu-id="016b0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="016b0-137">OUTPUTS</span></span>

### <span data-ttu-id="016b0-138">bool</span><span class="sxs-lookup"><span data-stu-id="016b0-138">bool</span></span>
<span data-ttu-id="016b0-139">Se PassThru è specificato, restituisce vero al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="016b0-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="016b0-140">Note</span><span class="sxs-lookup"><span data-stu-id="016b0-140">NOTES</span></span>

## <span data-ttu-id="016b0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="016b0-141">RELATED LINKS</span></span>

