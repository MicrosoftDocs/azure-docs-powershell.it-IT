---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: f9d0ee722f828aba251c9776c231338b54c0580c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673855"
---
# <span data-ttu-id="c80a8-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c80a8-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="c80a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c80a8-102">SYNOPSIS</span></span>
<span data-ttu-id="c80a8-103">Rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="c80a8-103">Removes a media service.</span></span>

## <span data-ttu-id="c80a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c80a8-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c80a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c80a8-105">DESCRIPTION</span></span>
<span data-ttu-id="c80a8-106">Il cmdlet **Remove-AzMediaService** rimuove un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="c80a8-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="c80a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c80a8-107">EXAMPLES</span></span>

### <span data-ttu-id="c80a8-108">Esempio 1: rimuovere un servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="c80a8-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="c80a8-109">Questo comando rimuove il servizio multimediale denominato MediaService0011 nel gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="c80a8-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="c80a8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c80a8-110">PARAMETERS</span></span>

### <span data-ttu-id="c80a8-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c80a8-111">-AccountName</span></span>
<span data-ttu-id="c80a8-112">Specifica il nome del servizio multimediale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c80a8-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c80a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80a8-113">-DefaultProfile</span></span>
<span data-ttu-id="c80a8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c80a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c80a8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c80a8-115">-Force</span></span>
<span data-ttu-id="c80a8-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c80a8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c80a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c80a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="c80a8-118">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="c80a8-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="c80a8-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c80a8-119">-Confirm</span></span>
<span data-ttu-id="c80a8-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c80a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c80a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c80a8-121">-WhatIf</span></span>
<span data-ttu-id="c80a8-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c80a8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c80a8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c80a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c80a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80a8-124">CommonParameters</span></span>
<span data-ttu-id="c80a8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c80a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80a8-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c80a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80a8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c80a8-127">INPUTS</span></span>

### <span data-ttu-id="c80a8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c80a8-128">System.String</span></span>

## <span data-ttu-id="c80a8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c80a8-129">OUTPUTS</span></span>

### <span data-ttu-id="c80a8-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c80a8-130">System.Boolean</span></span>

## <span data-ttu-id="c80a8-131">Note</span><span class="sxs-lookup"><span data-stu-id="c80a8-131">NOTES</span></span>

## <span data-ttu-id="c80a8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c80a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="c80a8-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c80a8-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="c80a8-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c80a8-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="c80a8-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c80a8-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


