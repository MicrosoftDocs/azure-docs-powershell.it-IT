---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: d035890f6478c0b7fd767f12b8f9a27d4f765837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673853"
---
# <span data-ttu-id="3ef37-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3ef37-101">Set-AzMediaService</span></span>

## <span data-ttu-id="3ef37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ef37-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef37-103">Modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="3ef37-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="3ef37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ef37-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ef37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ef37-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef37-106">Il cmdlet **set-AzMediaService** modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="3ef37-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="3ef37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ef37-107">EXAMPLES</span></span>

### <span data-ttu-id="3ef37-108">Esempio 1: modificare un servizio multimediale esistente</span><span class="sxs-lookup"><span data-stu-id="3ef37-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="3ef37-109">Il primo comando crea una serie di tag e archivia questi tag nella variabile denominata $Tags.</span><span class="sxs-lookup"><span data-stu-id="3ef37-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="3ef37-110">Questo secondo comando Aggiorna il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup123 con i tag archiviati in $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="3ef37-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="3ef37-111">Il comando usa inoltre una matrice di oggetti di configurazione dello spazio di archiviazione archiviati in $StorageAccounts variabile.</span><span class="sxs-lookup"><span data-stu-id="3ef37-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="3ef37-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ef37-112">PARAMETERS</span></span>

### <span data-ttu-id="3ef37-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ef37-113">-AccountName</span></span>
<span data-ttu-id="3ef37-114">Specifica il nome del servizio multimediale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ef37-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef37-115">-DefaultProfile</span></span>
<span data-ttu-id="3ef37-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ef37-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ef37-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef37-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ef37-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="3ef37-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="3ef37-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3ef37-119">-StorageAccounts</span></span>
<span data-ttu-id="3ef37-120">Specifica una matrice di account di archiviazione che il cmdlet associa al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="3ef37-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef37-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ef37-121">-Tag</span></span>
<span data-ttu-id="3ef37-122">Tag associati all'account multimediale.</span><span class="sxs-lookup"><span data-stu-id="3ef37-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef37-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ef37-123">-Confirm</span></span>
<span data-ttu-id="3ef37-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ef37-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ef37-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef37-125">-WhatIf</span></span>
<span data-ttu-id="3ef37-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ef37-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ef37-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ef37-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ef37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef37-128">CommonParameters</span></span>
<span data-ttu-id="3ef37-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef37-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef37-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef37-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ef37-131">INPUTS</span></span>

### <span data-ttu-id="3ef37-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3ef37-132">System.String</span></span>

### <span data-ttu-id="3ef37-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ef37-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3ef37-134">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="3ef37-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="3ef37-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ef37-135">OUTPUTS</span></span>

### <span data-ttu-id="3ef37-136">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="3ef37-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="3ef37-137">Note</span><span class="sxs-lookup"><span data-stu-id="3ef37-137">NOTES</span></span>

## <span data-ttu-id="3ef37-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ef37-138">RELATED LINKS</span></span>

[<span data-ttu-id="3ef37-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3ef37-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="3ef37-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3ef37-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="3ef37-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3ef37-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


