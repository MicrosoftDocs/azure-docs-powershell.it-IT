---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 7b8c1b154a631a911100f4b2b8581ca552e4b565
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520507"
---
# <span data-ttu-id="971ed-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="971ed-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="971ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="971ed-102">SYNOPSIS</span></span>
<span data-ttu-id="971ed-103">Rigenera una chiave usata per accedere all'endpoint REST associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="971ed-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="971ed-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="971ed-105">DESCRIPTION</span></span>
<span data-ttu-id="971ed-106">Il cmdlet **set-AzureRmMediaServiceKey** rigenera una chiave usata per accedere all'endpoint REST (Representational State Transfer) associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="971ed-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="971ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="971ed-107">EXAMPLES</span></span>

### <span data-ttu-id="971ed-108">Esempio 1: rigenerare la chiave primaria usata per l'accesso al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="971ed-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="971ed-109">Questo comando rigenera la chiave primaria per il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="971ed-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="971ed-110">Esempio 2: rigenera la chiave secondaria usata per accedere al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="971ed-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="971ed-111">Questo comando rigenera la chiave secondaria per il servizio multimediale denominato MediaService002 che appartiene al gruppo di risorse denominato Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="971ed-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="971ed-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="971ed-112">PARAMETERS</span></span>

### <span data-ttu-id="971ed-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="971ed-113">-AccountName</span></span>
<span data-ttu-id="971ed-114">Specifica il nome del servizio multimediale che questo cmdlet rigenera.</span><span class="sxs-lookup"><span data-stu-id="971ed-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="971ed-115">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="971ed-115">-KeyType</span></span>
<span data-ttu-id="971ed-116">Specifica il tipo di chiave del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="971ed-116">Specifies the key type of the media service.</span></span>
<span data-ttu-id="971ed-117">I valori accettabili per questo parametro sono: primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="971ed-117">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971ed-118">-ResourceGroupName</span></span>
<span data-ttu-id="971ed-119">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="971ed-119">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="971ed-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="971ed-120">-Confirm</span></span>
<span data-ttu-id="971ed-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="971ed-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971ed-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971ed-122">-WhatIf</span></span>
<span data-ttu-id="971ed-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="971ed-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="971ed-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="971ed-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971ed-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971ed-125">-DefaultProfile</span></span>
<span data-ttu-id="971ed-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="971ed-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971ed-127">CommonParameters</span></span>
<span data-ttu-id="971ed-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="971ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971ed-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="971ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971ed-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="971ed-130">INPUTS</span></span>

## <span data-ttu-id="971ed-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="971ed-131">OUTPUTS</span></span>

### <span data-ttu-id="971ed-132">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="971ed-132">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="971ed-133">Note</span><span class="sxs-lookup"><span data-stu-id="971ed-133">NOTES</span></span>

## <span data-ttu-id="971ed-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="971ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="971ed-135">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="971ed-135">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


