---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: e92bdaae728031ba38fc1326ac2abb29aac86c59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191138"
---
# <span data-ttu-id="ca3d3-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca3d3-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="ca3d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3d3-103">Rimuove un account di archiviazione da Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="ca3d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca3d3-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca3d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca3d3-105">DESCRIPTION</span></span>
<span data-ttu-id="ca3d3-106">Il cmdlet **Remove-AzStorageAccount** rimuove un account di archiviazione da Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="ca3d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca3d3-107">EXAMPLES</span></span>

### <span data-ttu-id="ca3d3-108">Esempio 1: rimuovere un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ca3d3-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="ca3d3-109">Questo comando rimuove l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="ca3d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca3d3-110">PARAMETERS</span></span>

### <span data-ttu-id="ca3d3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca3d3-111">-AsJob</span></span>
<span data-ttu-id="ca3d3-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca3d3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca3d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3d3-113">-DefaultProfile</span></span>
<span data-ttu-id="ca3d3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca3d3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca3d3-115">-Force</span></span>
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

### <span data-ttu-id="ca3d3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca3d3-116">-Name</span></span>
<span data-ttu-id="ca3d3-117">Specifica il nome dell'account di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca3d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="ca3d3-119">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="ca3d3-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca3d3-120">-Confirm</span></span>
<span data-ttu-id="ca3d3-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3d3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3d3-122">-WhatIf</span></span>
<span data-ttu-id="ca3d3-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca3d3-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3d3-125">CommonParameters</span></span>
<span data-ttu-id="ca3d3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca3d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3d3-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca3d3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3d3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca3d3-128">INPUTS</span></span>

### <span data-ttu-id="ca3d3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ca3d3-129">System.String</span></span>

## <span data-ttu-id="ca3d3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca3d3-130">OUTPUTS</span></span>

### <span data-ttu-id="ca3d3-131">System. void</span><span class="sxs-lookup"><span data-stu-id="ca3d3-131">System.Void</span></span>

## <span data-ttu-id="ca3d3-132">Note</span><span class="sxs-lookup"><span data-stu-id="ca3d3-132">NOTES</span></span>

## <span data-ttu-id="ca3d3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca3d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="ca3d3-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca3d3-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="ca3d3-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca3d3-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="ca3d3-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ca3d3-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


