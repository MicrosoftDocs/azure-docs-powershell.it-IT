---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 3dfa3343edc82aaaf2c51a4e18ebc413ea3023c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515124"
---
# <span data-ttu-id="b8af5-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b8af5-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="b8af5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8af5-102">SYNOPSIS</span></span>
<span data-ttu-id="b8af5-103">Modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="b8af5-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8af5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8af5-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8af5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8af5-105">DESCRIPTION</span></span>
<span data-ttu-id="b8af5-106">Il cmdlet **set-AzureRmMediaService** modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="b8af5-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="b8af5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8af5-107">EXAMPLES</span></span>

### <span data-ttu-id="b8af5-108">Esempio 1: modificare un servizio multimediale esistente</span><span class="sxs-lookup"><span data-stu-id="b8af5-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="b8af5-109">Il primo comando crea una serie di tag e archivia questi tag nella variabile denominata $Tags.</span><span class="sxs-lookup"><span data-stu-id="b8af5-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="b8af5-110">Questo secondo comando Aggiorna il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup123 con i tag archiviati in $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="b8af5-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="b8af5-111">Il comando usa inoltre una matrice di oggetti di configurazione dello spazio di archiviazione archiviati in $StorageAccounts variabile.</span><span class="sxs-lookup"><span data-stu-id="b8af5-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="b8af5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8af5-112">PARAMETERS</span></span>

### <span data-ttu-id="b8af5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b8af5-113">-AccountName</span></span>
<span data-ttu-id="b8af5-114">Specifica il nome del servizio multimediale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8af5-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b8af5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8af5-115">-DefaultProfile</span></span>
<span data-ttu-id="b8af5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b8af5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8af5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8af5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8af5-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b8af5-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b8af5-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b8af5-119">-StorageAccounts</span></span>
<span data-ttu-id="b8af5-120">Specifica una matrice di account di archiviazione che il cmdlet associa al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b8af5-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="b8af5-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8af5-121">-Tag</span></span>
<span data-ttu-id="b8af5-122">Tag associati all'account multimediale.</span><span class="sxs-lookup"><span data-stu-id="b8af5-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="b8af5-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b8af5-123">-Confirm</span></span>
<span data-ttu-id="b8af5-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8af5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8af5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8af5-125">-WhatIf</span></span>
<span data-ttu-id="b8af5-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8af5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8af5-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8af5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8af5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8af5-128">CommonParameters</span></span>
<span data-ttu-id="b8af5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8af5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8af5-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8af5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8af5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8af5-131">INPUTS</span></span>

### <span data-ttu-id="b8af5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b8af5-132">System.String</span></span>

### <span data-ttu-id="b8af5-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b8af5-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b8af5-134">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="b8af5-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="b8af5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8af5-135">OUTPUTS</span></span>

### <span data-ttu-id="b8af5-136">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="b8af5-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="b8af5-137">Note</span><span class="sxs-lookup"><span data-stu-id="b8af5-137">NOTES</span></span>

## <span data-ttu-id="b8af5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8af5-138">RELATED LINKS</span></span>

[<span data-ttu-id="b8af5-139">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b8af5-139">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="b8af5-140">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b8af5-140">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="b8af5-141">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b8af5-141">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


