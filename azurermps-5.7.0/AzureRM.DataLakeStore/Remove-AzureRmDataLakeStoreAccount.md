---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 4e21d122c8a49209a7591457c36ba99fcc10496c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509875"
---
# <span data-ttu-id="c037d-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c037d-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="c037d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c037d-102">SYNOPSIS</span></span>
<span data-ttu-id="c037d-103">Elimina definitivamente un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c037d-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c037d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c037d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c037d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c037d-105">DESCRIPTION</span></span>
<span data-ttu-id="c037d-106">Il cmdlet **Remove-AzureRmDataLakeStoreAccount** Elimina definitivamente un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c037d-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="c037d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c037d-107">EXAMPLES</span></span>

### <span data-ttu-id="c037d-108">Esempio 1: rimuovere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c037d-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="c037d-109">Questo comando rimuove l'account denominato ContosoADL da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c037d-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="c037d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c037d-110">PARAMETERS</span></span>

### <span data-ttu-id="c037d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c037d-111">-DefaultProfile</span></span>
<span data-ttu-id="c037d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c037d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c037d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c037d-113">-Force</span></span>
<span data-ttu-id="c037d-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c037d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c037d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c037d-115">-Name</span></span>
<span data-ttu-id="c037d-116">Specifica il nome dell'account da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c037d-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="c037d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c037d-117">-PassThru</span></span>
<span data-ttu-id="c037d-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c037d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c037d-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c037d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c037d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c037d-120">-ResourceGroupName</span></span>
<span data-ttu-id="c037d-121">Specifica il gruppo di risorse che contiene l'account da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c037d-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="c037d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c037d-122">-Confirm</span></span>
<span data-ttu-id="c037d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c037d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c037d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c037d-124">-WhatIf</span></span>
<span data-ttu-id="c037d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c037d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c037d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c037d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c037d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c037d-127">CommonParameters</span></span>
<span data-ttu-id="c037d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c037d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c037d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c037d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c037d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c037d-130">INPUTS</span></span>

### <span data-ttu-id="c037d-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c037d-131">None</span></span>
<span data-ttu-id="c037d-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c037d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c037d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c037d-133">OUTPUTS</span></span>

### <span data-ttu-id="c037d-134">bool</span><span class="sxs-lookup"><span data-stu-id="c037d-134">bool</span></span>
<span data-ttu-id="c037d-135">Se PassThru è specificato, restituisce vero al completamento corretto.</span><span class="sxs-lookup"><span data-stu-id="c037d-135">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="c037d-136">Note</span><span class="sxs-lookup"><span data-stu-id="c037d-136">NOTES</span></span>

## <span data-ttu-id="c037d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c037d-137">RELATED LINKS</span></span>

[<span data-ttu-id="c037d-138">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c037d-138">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c037d-139">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c037d-139">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c037d-140">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c037d-140">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c037d-141">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c037d-141">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


