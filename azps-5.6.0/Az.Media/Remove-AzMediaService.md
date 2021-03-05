---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 5b27574dc6ea60472a16c0b647027ceba17a87b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006589"
---
# <span data-ttu-id="2fdaa-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2fdaa-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="2fdaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fdaa-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdaa-103">Rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-103">Removes a media service.</span></span>

## <span data-ttu-id="2fdaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fdaa-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fdaa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2fdaa-105">DESCRIPTION</span></span>
<span data-ttu-id="2fdaa-106">Il cmdlet **Remove-AzMediaService** rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="2fdaa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fdaa-107">EXAMPLES</span></span>

### <span data-ttu-id="2fdaa-108">Esempio 1: Rimuovere un servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="2fdaa-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="2fdaa-109">Questo comando rimuove il servizio multimediale denominato MediaService0011 nel gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="2fdaa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fdaa-110">PARAMETERS</span></span>

### <span data-ttu-id="2fdaa-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2fdaa-111">-AccountName</span></span>
<span data-ttu-id="2fdaa-112">Specifica il nome del servizio multimediale rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2fdaa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdaa-113">-DefaultProfile</span></span>
<span data-ttu-id="2fdaa-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2fdaa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fdaa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2fdaa-115">-Force</span></span>
<span data-ttu-id="2fdaa-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fdaa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdaa-117">-ResourceGroupName</span></span>
<span data-ttu-id="2fdaa-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="2fdaa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fdaa-119">-Confirm</span></span>
<span data-ttu-id="2fdaa-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdaa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdaa-121">-WhatIf</span></span>
<span data-ttu-id="2fdaa-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fdaa-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdaa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdaa-124">CommonParameters</span></span>
<span data-ttu-id="2fdaa-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fdaa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdaa-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdaa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdaa-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="2fdaa-127">INPUTS</span></span>

### <span data-ttu-id="2fdaa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2fdaa-128">System.String</span></span>

## <span data-ttu-id="2fdaa-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fdaa-129">OUTPUTS</span></span>

### <span data-ttu-id="2fdaa-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2fdaa-130">System.Boolean</span></span>

## <span data-ttu-id="2fdaa-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="2fdaa-131">NOTES</span></span>

## <span data-ttu-id="2fdaa-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fdaa-132">RELATED LINKS</span></span>

[<span data-ttu-id="2fdaa-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2fdaa-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="2fdaa-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2fdaa-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="2fdaa-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2fdaa-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


