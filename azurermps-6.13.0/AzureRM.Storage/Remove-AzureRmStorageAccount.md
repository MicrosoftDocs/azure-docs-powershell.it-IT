---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: 9c512c1993700e1bbdab4d5c0d52a1aa2ceeafb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521291"
---
# <span data-ttu-id="19cef-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19cef-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="19cef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19cef-102">SYNOPSIS</span></span>
<span data-ttu-id="19cef-103">Rimuove un account di archiviazione da Azure.</span><span class="sxs-lookup"><span data-stu-id="19cef-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19cef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19cef-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19cef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19cef-105">DESCRIPTION</span></span>
<span data-ttu-id="19cef-106">Il cmdlet **Remove-AzureRmStorageAccount** rimuove un account di archiviazione da Azure.</span><span class="sxs-lookup"><span data-stu-id="19cef-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="19cef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19cef-107">EXAMPLES</span></span>

### <span data-ttu-id="19cef-108">Esempio 1: rimuovere un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="19cef-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="19cef-109">Questo comando rimuove l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="19cef-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="19cef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19cef-110">PARAMETERS</span></span>

### <span data-ttu-id="19cef-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19cef-111">-AsJob</span></span>
<span data-ttu-id="19cef-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="19cef-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19cef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cef-113">-DefaultProfile</span></span>
<span data-ttu-id="19cef-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19cef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19cef-115">-Force</span><span class="sxs-lookup"><span data-stu-id="19cef-115">-Force</span></span>
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

### <span data-ttu-id="19cef-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="19cef-116">-Name</span></span>
<span data-ttu-id="19cef-117">Specifica il nome dell'account di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="19cef-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="19cef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19cef-118">-ResourceGroupName</span></span>
<span data-ttu-id="19cef-119">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="19cef-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="19cef-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19cef-120">-Confirm</span></span>
<span data-ttu-id="19cef-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19cef-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19cef-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19cef-122">-WhatIf</span></span>
<span data-ttu-id="19cef-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19cef-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19cef-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19cef-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19cef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cef-125">CommonParameters</span></span>
<span data-ttu-id="19cef-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19cef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cef-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cef-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19cef-128">INPUTS</span></span>

### <span data-ttu-id="19cef-129">System. String</span><span class="sxs-lookup"><span data-stu-id="19cef-129">System.String</span></span>

## <span data-ttu-id="19cef-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19cef-130">OUTPUTS</span></span>

### <span data-ttu-id="19cef-131">System. void</span><span class="sxs-lookup"><span data-stu-id="19cef-131">System.Void</span></span>

## <span data-ttu-id="19cef-132">Note</span><span class="sxs-lookup"><span data-stu-id="19cef-132">NOTES</span></span>

## <span data-ttu-id="19cef-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19cef-133">RELATED LINKS</span></span>

[<span data-ttu-id="19cef-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19cef-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="19cef-135">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19cef-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="19cef-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19cef-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


