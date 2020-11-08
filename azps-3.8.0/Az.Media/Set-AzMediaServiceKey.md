---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 0a7dc826aae7efebfc3d24bdeba02c75d0bf5a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022482"
---
# <span data-ttu-id="5e644-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="5e644-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="5e644-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e644-102">SYNOPSIS</span></span>
<span data-ttu-id="5e644-103">Rigenera una chiave usata per accedere all'endpoint REST associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="5e644-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="5e644-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e644-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e644-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e644-105">DESCRIPTION</span></span>
<span data-ttu-id="5e644-106">Il cmdlet **set-AzMediaServiceKey** rigenera una chiave usata per accedere all'endpoint REST (Representational State Transfer) associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="5e644-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="5e644-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e644-107">EXAMPLES</span></span>

### <span data-ttu-id="5e644-108">Esempio 1: rigenerare la chiave primaria usata per l'accesso al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="5e644-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="5e644-109">Questo comando rigenera la chiave primaria per il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="5e644-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="5e644-110">Esempio 2: rigenera la chiave secondaria usata per accedere al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="5e644-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="5e644-111">Questo comando rigenera la chiave secondaria per il servizio multimediale denominato MediaService002 che appartiene al gruppo di risorse denominato Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="5e644-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="5e644-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e644-112">PARAMETERS</span></span>

### <span data-ttu-id="5e644-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e644-113">-AccountName</span></span>
<span data-ttu-id="5e644-114">Specifica il nome del servizio multimediale che questo cmdlet rigenera.</span><span class="sxs-lookup"><span data-stu-id="5e644-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="5e644-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e644-115">-DefaultProfile</span></span>
<span data-ttu-id="5e644-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5e644-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e644-117">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="5e644-117">-KeyType</span></span>
<span data-ttu-id="5e644-118">Specifica il tipo di chiave del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="5e644-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="5e644-119">I valori accettabili per questo parametro sono: primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="5e644-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="5e644-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e644-120">-ResourceGroupName</span></span>
<span data-ttu-id="5e644-121">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="5e644-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="5e644-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e644-122">-Confirm</span></span>
<span data-ttu-id="5e644-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e644-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e644-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e644-124">-WhatIf</span></span>
<span data-ttu-id="5e644-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e644-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e644-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e644-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e644-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e644-127">CommonParameters</span></span>
<span data-ttu-id="5e644-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e644-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e644-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e644-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e644-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e644-130">INPUTS</span></span>

### <span data-ttu-id="5e644-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5e644-131">System.String</span></span>

## <span data-ttu-id="5e644-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e644-132">OUTPUTS</span></span>

### <span data-ttu-id="5e644-133">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="5e644-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="5e644-134">Note</span><span class="sxs-lookup"><span data-stu-id="5e644-134">NOTES</span></span>

## <span data-ttu-id="5e644-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e644-135">RELATED LINKS</span></span>

[<span data-ttu-id="5e644-136">Get-AzMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="5e644-136">Get-AzMediaServiceKeys</span></span>](./Get-AzMediaServiceKeys.md)


