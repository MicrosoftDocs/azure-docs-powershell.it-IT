---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191618"
---
# <span data-ttu-id="a20ad-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a20ad-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a20ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a20ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a20ad-103">Elimina un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="a20ad-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a20ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a20ad-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20ad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a20ad-105">DESCRIPTION</span></span>
<span data-ttu-id="a20ad-106">Il cmdlet **Remove-AzDataLakeAnalyticsAccount** Elimina definitivamente un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a20ad-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a20ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a20ad-107">EXAMPLES</span></span>

### <span data-ttu-id="a20ad-108">Esempio 1: rimuovere un account</span><span class="sxs-lookup"><span data-stu-id="a20ad-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="a20ad-109">Questo comando rimuove l'account di analisi dei dati del lago specificato.</span><span class="sxs-lookup"><span data-stu-id="a20ad-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="a20ad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a20ad-110">PARAMETERS</span></span>

### <span data-ttu-id="a20ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20ad-111">-DefaultProfile</span></span>
<span data-ttu-id="a20ad-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a20ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a20ad-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a20ad-113">-Force</span></span>
<span data-ttu-id="a20ad-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a20ad-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a20ad-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a20ad-115">-Name</span></span>
<span data-ttu-id="a20ad-116">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="a20ad-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a20ad-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a20ad-117">-PassThru</span></span>
<span data-ttu-id="a20ad-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a20ad-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a20ad-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a20ad-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a20ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="a20ad-121">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="a20ad-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a20ad-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a20ad-122">-Confirm</span></span>
<span data-ttu-id="a20ad-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a20ad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20ad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20ad-124">-WhatIf</span></span>
<span data-ttu-id="a20ad-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a20ad-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20ad-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a20ad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20ad-127">CommonParameters</span></span>
<span data-ttu-id="a20ad-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20ad-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20ad-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20ad-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a20ad-130">INPUTS</span></span>

### <span data-ttu-id="a20ad-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a20ad-131">System.String</span></span>

## <span data-ttu-id="a20ad-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a20ad-132">OUTPUTS</span></span>

### <span data-ttu-id="a20ad-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a20ad-133">System.Boolean</span></span>

## <span data-ttu-id="a20ad-134">Note</span><span class="sxs-lookup"><span data-stu-id="a20ad-134">NOTES</span></span>

## <span data-ttu-id="a20ad-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a20ad-135">RELATED LINKS</span></span>

[<span data-ttu-id="a20ad-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a20ad-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a20ad-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a20ad-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a20ad-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a20ad-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a20ad-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a20ad-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


