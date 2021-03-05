---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 410b1c87832b4debdfd50cbe6adf27326f12a303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982990"
---
# <span data-ttu-id="85e64-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="85e64-101">Set-AzMediaService</span></span>

## <span data-ttu-id="85e64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85e64-102">SYNOPSIS</span></span>
<span data-ttu-id="85e64-103">Modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="85e64-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="85e64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85e64-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85e64-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85e64-105">DESCRIPTION</span></span>
<span data-ttu-id="85e64-106">Il cmdlet **Set-AzMediaService** modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="85e64-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="85e64-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85e64-107">EXAMPLES</span></span>

### <span data-ttu-id="85e64-108">Esempio 1: Modificare un servizio multimediale esistente</span><span class="sxs-lookup"><span data-stu-id="85e64-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="85e64-109">Il primo comando crea una serie di tag e li archivia nella variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="85e64-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="85e64-110">Questo secondo comando aggiorna il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup123 con i tag archiviati in $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="85e64-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="85e64-111">Il comando usa anche una matrice di oggetti di configurazione di archiviazione archiviati in $StorageAccounts variabile.</span><span class="sxs-lookup"><span data-stu-id="85e64-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="85e64-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85e64-112">PARAMETERS</span></span>

### <span data-ttu-id="85e64-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85e64-113">-AccountName</span></span>
<span data-ttu-id="85e64-114">Specifica il nome del servizio multimediale modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85e64-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="85e64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e64-115">-DefaultProfile</span></span>
<span data-ttu-id="85e64-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="85e64-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85e64-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e64-117">-ResourceGroupName</span></span>
<span data-ttu-id="85e64-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="85e64-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="85e64-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="85e64-119">-StorageAccounts</span></span>
<span data-ttu-id="85e64-120">Specifica una matrice di account di archiviazione che questo cmdlet associa al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="85e64-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="85e64-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="85e64-121">-Tag</span></span>
<span data-ttu-id="85e64-122">I tag associati all'account multimediale.</span><span class="sxs-lookup"><span data-stu-id="85e64-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="85e64-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85e64-123">-Confirm</span></span>
<span data-ttu-id="85e64-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85e64-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85e64-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85e64-125">-WhatIf</span></span>
<span data-ttu-id="85e64-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85e64-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85e64-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85e64-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85e64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e64-128">CommonParameters</span></span>
<span data-ttu-id="85e64-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e64-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e64-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e64-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="85e64-131">INPUTS</span></span>

### <span data-ttu-id="85e64-132">System.String</span><span class="sxs-lookup"><span data-stu-id="85e64-132">System.String</span></span>

### <span data-ttu-id="85e64-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="85e64-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="85e64-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="85e64-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="85e64-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85e64-135">OUTPUTS</span></span>

### <span data-ttu-id="85e64-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="85e64-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="85e64-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="85e64-137">NOTES</span></span>

## <span data-ttu-id="85e64-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85e64-138">RELATED LINKS</span></span>

[<span data-ttu-id="85e64-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="85e64-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="85e64-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="85e64-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="85e64-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="85e64-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


