---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203628"
---
# <span data-ttu-id="e670f-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e670f-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="e670f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e670f-102">SYNOPSIS</span></span>
<span data-ttu-id="e670f-103">Rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e670f-103">Removes a media service.</span></span>

## <span data-ttu-id="e670f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e670f-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e670f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e670f-105">DESCRIPTION</span></span>
<span data-ttu-id="e670f-106">Il cmdlet **Remove-AzMediaService** rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e670f-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="e670f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e670f-107">EXAMPLES</span></span>

### <span data-ttu-id="e670f-108">Esempio 1: Rimuovere un servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="e670f-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="e670f-109">Questo comando rimuove il servizio multimediale denominato MediaService0011 nel gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="e670f-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="e670f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e670f-110">PARAMETERS</span></span>

### <span data-ttu-id="e670f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e670f-111">-AccountName</span></span>
<span data-ttu-id="e670f-112">Specifica il nome del servizio multimediale rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e670f-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e670f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e670f-113">-DefaultProfile</span></span>
<span data-ttu-id="e670f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e670f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e670f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e670f-115">-Force</span></span>
<span data-ttu-id="e670f-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="e670f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e670f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e670f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e670f-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="e670f-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="e670f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e670f-119">-Confirm</span></span>
<span data-ttu-id="e670f-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e670f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e670f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e670f-121">-WhatIf</span></span>
<span data-ttu-id="e670f-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e670f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e670f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e670f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e670f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e670f-124">CommonParameters</span></span>
<span data-ttu-id="e670f-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e670f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e670f-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e670f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e670f-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e670f-127">INPUTS</span></span>

### <span data-ttu-id="e670f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e670f-128">System.String</span></span>

## <span data-ttu-id="e670f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e670f-129">OUTPUTS</span></span>

### <span data-ttu-id="e670f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e670f-130">System.Boolean</span></span>

## <span data-ttu-id="e670f-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="e670f-131">NOTES</span></span>

## <span data-ttu-id="e670f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e670f-132">RELATED LINKS</span></span>

[<span data-ttu-id="e670f-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e670f-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="e670f-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e670f-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="e670f-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e670f-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


