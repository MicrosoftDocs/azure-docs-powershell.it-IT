---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 85f8b91fd99da5d5b014d74ff8fadd225ab0c2c7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409274"
---
# <span data-ttu-id="9c404-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="9c404-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="9c404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c404-102">SYNOPSIS</span></span>
<span data-ttu-id="9c404-103">Rigenera una chiave usata per accedere all'endpoint REST associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="9c404-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="9c404-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c404-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c404-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c404-105">DESCRIPTION</span></span>
<span data-ttu-id="9c404-106">Il cmdlet **Set-AzMediaServiceKey** rigenera una chiave usata per accedere all'endpoint Representational State Transfer (REST) associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="9c404-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="9c404-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c404-107">EXAMPLES</span></span>

### <span data-ttu-id="9c404-108">Esempio 1: Rigenerare la chiave primaria usata per accedere al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="9c404-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="9c404-109">Questo comando rigenera la chiave primaria per il servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="9c404-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="9c404-110">Esempio 2: rigenera la chiave secondaria usata per accedere al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="9c404-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="9c404-111">Questo comando rigenera la chiave secondaria per il servizio multimediale denominato MediaService002 che appartiene al gruppo di risorse denominato Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="9c404-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="9c404-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c404-112">PARAMETERS</span></span>

### <span data-ttu-id="9c404-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c404-113">-AccountName</span></span>
<span data-ttu-id="9c404-114">Specifica il nome del servizio multimediale rigenerato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c404-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="9c404-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c404-115">-DefaultProfile</span></span>
<span data-ttu-id="9c404-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9c404-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c404-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9c404-117">-KeyType</span></span>
<span data-ttu-id="9c404-118">Specifica il tipo di chiave del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="9c404-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="9c404-119">I valori accettabili per questo parametro sono: Primario o Secondario.</span><span class="sxs-lookup"><span data-stu-id="9c404-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="9c404-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c404-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c404-121">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="9c404-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="9c404-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c404-122">-Confirm</span></span>
<span data-ttu-id="9c404-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c404-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c404-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c404-124">-WhatIf</span></span>
<span data-ttu-id="9c404-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c404-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c404-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c404-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c404-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c404-127">CommonParameters</span></span>
<span data-ttu-id="9c404-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c404-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c404-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c404-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c404-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c404-130">INPUTS</span></span>

### <span data-ttu-id="9c404-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9c404-131">System.String</span></span>

## <span data-ttu-id="9c404-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c404-132">OUTPUTS</span></span>

### <span data-ttu-id="9c404-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="9c404-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="9c404-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c404-134">NOTES</span></span>

## <span data-ttu-id="9c404-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c404-135">RELATED LINKS</span></span>



