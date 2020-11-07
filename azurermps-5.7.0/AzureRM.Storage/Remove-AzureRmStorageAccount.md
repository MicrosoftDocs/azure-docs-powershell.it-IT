---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: e6a6a35b5e744218c3afc6db396e875ad0acf242
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687401"
---
# <span data-ttu-id="ae1a5-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae1a5-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="ae1a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1a5-103">Rimuove un account di archiviazione da Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae1a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae1a5-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae1a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae1a5-105">DESCRIPTION</span></span>
<span data-ttu-id="ae1a5-106">Il cmdlet **Remove-AzureRmStorageAccount** rimuove un account di archiviazione da Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="ae1a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae1a5-107">EXAMPLES</span></span>

### <span data-ttu-id="ae1a5-108">Esempio 1: rimuovere un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ae1a5-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="ae1a5-109">Questo comando rimuove l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="ae1a5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae1a5-110">PARAMETERS</span></span>

### <span data-ttu-id="ae1a5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ae1a5-111">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae1a5-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae1a5-112">-Name</span></span>
<span data-ttu-id="ae1a5-113">Specifica il nome dell'account di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-113">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1a5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae1a5-114">-ResourceGroupName</span></span>
<span data-ttu-id="ae1a5-115">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="ae1a5-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae1a5-116">-Confirm</span></span>
<span data-ttu-id="ae1a5-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae1a5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae1a5-118">-WhatIf</span></span>
<span data-ttu-id="ae1a5-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae1a5-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae1a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1a5-121">CommonParameters</span></span>
<span data-ttu-id="ae1a5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1a5-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1a5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1a5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae1a5-124">INPUTS</span></span>

### <span data-ttu-id="ae1a5-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ae1a5-125">None</span></span>
<span data-ttu-id="ae1a5-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae1a5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae1a5-127">OUTPUTS</span></span>

## <span data-ttu-id="ae1a5-128">Note</span><span class="sxs-lookup"><span data-stu-id="ae1a5-128">NOTES</span></span>

## <span data-ttu-id="ae1a5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae1a5-129">RELATED LINKS</span></span>

[<span data-ttu-id="ae1a5-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae1a5-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="ae1a5-131">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae1a5-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="ae1a5-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae1a5-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
