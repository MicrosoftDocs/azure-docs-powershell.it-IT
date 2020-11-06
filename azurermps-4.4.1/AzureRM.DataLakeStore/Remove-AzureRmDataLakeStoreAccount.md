---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519591"
---
# <span data-ttu-id="642a2-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="642a2-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="642a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="642a2-102">SYNOPSIS</span></span>
<span data-ttu-id="642a2-103">Elimina definitivamente un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="642a2-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="642a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="642a2-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="642a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="642a2-105">DESCRIPTION</span></span>
<span data-ttu-id="642a2-106">Il cmdlet **Remove-AzureRmDataLakeStoreAccount** Elimina definitivamente un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="642a2-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="642a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="642a2-107">EXAMPLES</span></span>

### <span data-ttu-id="642a2-108">Esempio 1: rimuovere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="642a2-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="642a2-109">Questo comando rimuove l'account denominato ContosoADL da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="642a2-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="642a2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="642a2-110">PARAMETERS</span></span>

### <span data-ttu-id="642a2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="642a2-111">-Force</span></span>
<span data-ttu-id="642a2-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="642a2-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="642a2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="642a2-113">-Name</span></span>
<span data-ttu-id="642a2-114">Specifica il nome dell'account da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="642a2-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="642a2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="642a2-115">-PassThru</span></span>
<span data-ttu-id="642a2-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="642a2-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="642a2-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="642a2-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="642a2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642a2-118">-ResourceGroupName</span></span>
<span data-ttu-id="642a2-119">Specifica il gruppo di risorse che contiene l'account da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="642a2-119">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="642a2-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="642a2-120">-Confirm</span></span>
<span data-ttu-id="642a2-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="642a2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642a2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642a2-122">-WhatIf</span></span>
<span data-ttu-id="642a2-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="642a2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="642a2-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="642a2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642a2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642a2-125">-DefaultProfile</span></span>
<span data-ttu-id="642a2-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="642a2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="642a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642a2-127">CommonParameters</span></span>
<span data-ttu-id="642a2-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="642a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642a2-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="642a2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642a2-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="642a2-130">INPUTS</span></span>

## <span data-ttu-id="642a2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="642a2-131">OUTPUTS</span></span>

### <span data-ttu-id="642a2-132">bool</span><span class="sxs-lookup"><span data-stu-id="642a2-132">bool</span></span>
<span data-ttu-id="642a2-133">Se PassThru è specificato, restituisce vero al completamento corretto.</span><span class="sxs-lookup"><span data-stu-id="642a2-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="642a2-134">Note</span><span class="sxs-lookup"><span data-stu-id="642a2-134">NOTES</span></span>

## <span data-ttu-id="642a2-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="642a2-135">RELATED LINKS</span></span>

[<span data-ttu-id="642a2-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="642a2-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="642a2-137">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="642a2-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="642a2-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="642a2-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="642a2-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="642a2-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


