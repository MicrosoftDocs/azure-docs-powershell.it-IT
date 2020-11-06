---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 373647cfc06c36a510a8208424d00087f00e693e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508112"
---
# <span data-ttu-id="d83fb-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d83fb-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="d83fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d83fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d83fb-103">Rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="d83fb-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d83fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d83fb-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d83fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d83fb-105">DESCRIPTION</span></span>
<span data-ttu-id="d83fb-106">Il cmdlet **Remove-AzureRmMediaService** rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="d83fb-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="d83fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d83fb-107">EXAMPLES</span></span>

### <span data-ttu-id="d83fb-108">Esempio 1: rimuovere un servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="d83fb-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="d83fb-109">Questo comando rimuove il servizio multimediale denominato MediaService0011 nel gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="d83fb-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="d83fb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d83fb-110">PARAMETERS</span></span>

### <span data-ttu-id="d83fb-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d83fb-111">-AccountName</span></span>
<span data-ttu-id="d83fb-112">Specifica il nome del servizio multimediale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d83fb-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d83fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83fb-113">-DefaultProfile</span></span>
<span data-ttu-id="d83fb-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d83fb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d83fb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d83fb-115">-Force</span></span>
<span data-ttu-id="d83fb-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d83fb-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d83fb-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="d83fb-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d83fb-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d83fb-119">-Confirm</span></span>
<span data-ttu-id="d83fb-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d83fb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d83fb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d83fb-121">-WhatIf</span></span>
<span data-ttu-id="d83fb-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d83fb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d83fb-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d83fb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d83fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83fb-124">CommonParameters</span></span>
<span data-ttu-id="d83fb-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83fb-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83fb-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d83fb-127">INPUTS</span></span>

### <span data-ttu-id="d83fb-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d83fb-128">None</span></span>
<span data-ttu-id="d83fb-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d83fb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d83fb-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d83fb-130">OUTPUTS</span></span>

### <span data-ttu-id="d83fb-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d83fb-131">System.Boolean</span></span>

## <span data-ttu-id="d83fb-132">Note</span><span class="sxs-lookup"><span data-stu-id="d83fb-132">NOTES</span></span>

## <span data-ttu-id="d83fb-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d83fb-133">RELATED LINKS</span></span>

[<span data-ttu-id="d83fb-134">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d83fb-134">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="d83fb-135">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d83fb-135">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="d83fb-136">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="d83fb-136">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


