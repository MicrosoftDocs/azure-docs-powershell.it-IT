---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 19db06ff5563e954124ab36274d62cce0e51b3a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519569"
---
# <span data-ttu-id="89f97-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="89f97-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="89f97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89f97-102">SYNOPSIS</span></span>
<span data-ttu-id="89f97-103">Modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="89f97-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89f97-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tags <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89f97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89f97-105">DESCRIPTION</span></span>
<span data-ttu-id="89f97-106">Il cmdlet **set-AzureRmMediaService** modifica le proprietà specificate di un servizio multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="89f97-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="89f97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89f97-107">EXAMPLES</span></span>

### <span data-ttu-id="89f97-108">Esempio 1: modificare un servizio multimediale esistente</span><span class="sxs-lookup"><span data-stu-id="89f97-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="89f97-109">Il primo comando crea una serie di tag e archivia questi tag nella variabile denominata $Tags.</span><span class="sxs-lookup"><span data-stu-id="89f97-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="89f97-110">Questo secondo comando Aggiorna il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup123 con i tag archiviati in $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="89f97-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="89f97-111">Il comando usa inoltre una matrice di oggetti di configurazione dello spazio di archiviazione archiviati in $StorageAccounts variabile.</span><span class="sxs-lookup"><span data-stu-id="89f97-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="89f97-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89f97-112">PARAMETERS</span></span>

### <span data-ttu-id="89f97-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89f97-113">-AccountName</span></span>
<span data-ttu-id="89f97-114">Specifica il nome del servizio multimediale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f97-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="89f97-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f97-115">-ResourceGroupName</span></span>
<span data-ttu-id="89f97-116">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="89f97-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="89f97-117">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="89f97-117">-StorageAccounts</span></span>
<span data-ttu-id="89f97-118">Specifica una matrice di account di archiviazione che il cmdlet associa al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="89f97-118">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="89f97-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="89f97-119">-Tags</span></span>
<span data-ttu-id="89f97-120">Specifica i contrassegni per il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="89f97-120">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="89f97-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89f97-121">-Confirm</span></span>
<span data-ttu-id="89f97-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89f97-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f97-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f97-123">-WhatIf</span></span>
<span data-ttu-id="89f97-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89f97-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f97-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89f97-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f97-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f97-126">-DefaultProfile</span></span>
<span data-ttu-id="89f97-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89f97-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89f97-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f97-128">CommonParameters</span></span>
<span data-ttu-id="89f97-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f97-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f97-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f97-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f97-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89f97-131">INPUTS</span></span>

## <span data-ttu-id="89f97-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89f97-132">OUTPUTS</span></span>

### <span data-ttu-id="89f97-133">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="89f97-133">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="89f97-134">Note</span><span class="sxs-lookup"><span data-stu-id="89f97-134">NOTES</span></span>

## <span data-ttu-id="89f97-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89f97-135">RELATED LINKS</span></span>

[<span data-ttu-id="89f97-136">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="89f97-136">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="89f97-137">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="89f97-137">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="89f97-138">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="89f97-138">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


