---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 413a357d793bd72ff7d1e30cb65e56cb5bd5f3a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515640"
---
# <span data-ttu-id="9ed2c-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="9ed2c-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="9ed2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ed2c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed2c-103">Modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ed2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ed2c-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ed2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ed2c-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed2c-106">Il cmdlet **set-AzureRmMediaService** modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="9ed2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ed2c-107">EXAMPLES</span></span>

### <span data-ttu-id="9ed2c-108">Esempio 1: modificare un servizio multimediale esistente</span><span class="sxs-lookup"><span data-stu-id="9ed2c-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="9ed2c-109">Il primo comando crea una serie di tag e archivia questi tag nella variabile denominata $Tags.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="9ed2c-110">Questo secondo comando Aggiorna il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup123 con i tag archiviati in $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="9ed2c-111">Il comando usa inoltre una matrice di oggetti di configurazione dello spazio di archiviazione archiviati in $StorageAccounts variabile.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="9ed2c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ed2c-112">PARAMETERS</span></span>

### <span data-ttu-id="9ed2c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ed2c-113">-AccountName</span></span>
<span data-ttu-id="9ed2c-114">Specifica il nome del servizio multimediale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed2c-115">-DefaultProfile</span></span>
<span data-ttu-id="9ed2c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9ed2c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ed2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ed2c-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="9ed2c-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="9ed2c-119">-StorageAccounts</span></span>
<span data-ttu-id="9ed2c-120">Specifica una matrice di account di archiviazione che il cmdlet associa al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed2c-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ed2c-121">-Tag</span></span>
<span data-ttu-id="9ed2c-122">Tag associati all'account multimediale.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-122">The tags associated with the media account.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed2c-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ed2c-123">-Confirm</span></span>
<span data-ttu-id="9ed2c-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed2c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed2c-125">-WhatIf</span></span>
<span data-ttu-id="9ed2c-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed2c-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed2c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed2c-128">CommonParameters</span></span>
<span data-ttu-id="9ed2c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed2c-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed2c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed2c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ed2c-131">INPUTS</span></span>

### <span data-ttu-id="9ed2c-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9ed2c-132">None</span></span>
<span data-ttu-id="9ed2c-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9ed2c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ed2c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ed2c-134">OUTPUTS</span></span>

### <span data-ttu-id="9ed2c-135">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="9ed2c-135">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="9ed2c-136">Note</span><span class="sxs-lookup"><span data-stu-id="9ed2c-136">NOTES</span></span>

## <span data-ttu-id="9ed2c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ed2c-137">RELATED LINKS</span></span>

[<span data-ttu-id="9ed2c-138">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="9ed2c-138">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="9ed2c-139">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="9ed2c-139">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="9ed2c-140">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="9ed2c-140">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


