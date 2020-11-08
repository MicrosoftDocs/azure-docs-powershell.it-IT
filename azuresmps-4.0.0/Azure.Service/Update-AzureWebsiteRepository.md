---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023801"
---
# <span data-ttu-id="f15aa-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="f15aa-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="f15aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f15aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f15aa-103">Aggiorna i repository remoti di un repository git locale per tutti gli slot.</span><span class="sxs-lookup"><span data-stu-id="f15aa-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="f15aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f15aa-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f15aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f15aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f15aa-106">Il cmdlet **Update-AzureWebsiteRepository** aggiorna i repository remoti di un repository git locale per tutti gli slot.</span><span class="sxs-lookup"><span data-stu-id="f15aa-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="f15aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f15aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f15aa-108">Esempio 1: aggiornare i repository remoti del sito Web</span><span class="sxs-lookup"><span data-stu-id="f15aa-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="f15aa-109">Aggiorna i repository remoti di un repository git locale per tutti gli slot per il sito Web di website.</span><span class="sxs-lookup"><span data-stu-id="f15aa-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="f15aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f15aa-110">PARAMETERS</span></span>

### <span data-ttu-id="f15aa-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="f15aa-111">-Name</span></span>
<span data-ttu-id="f15aa-112">Nome del sito Web.</span><span class="sxs-lookup"><span data-stu-id="f15aa-112">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15aa-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="f15aa-113">-Profile</span></span>
<span data-ttu-id="f15aa-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f15aa-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f15aa-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f15aa-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f15aa-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="f15aa-116">-PublishingUsername</span></span>
<span data-ttu-id="f15aa-117">Nome utente specificato nel portale di Microsoft Azure per la distribuzione git.</span><span class="sxs-lookup"><span data-stu-id="f15aa-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f15aa-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f15aa-118">-Confirm</span></span>
<span data-ttu-id="f15aa-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f15aa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f15aa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f15aa-120">-WhatIf</span></span>
<span data-ttu-id="f15aa-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f15aa-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f15aa-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f15aa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f15aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15aa-123">CommonParameters</span></span>
<span data-ttu-id="f15aa-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f15aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15aa-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f15aa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15aa-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f15aa-126">INPUTS</span></span>

## <span data-ttu-id="f15aa-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f15aa-127">OUTPUTS</span></span>

## <span data-ttu-id="f15aa-128">Note</span><span class="sxs-lookup"><span data-stu-id="f15aa-128">NOTES</span></span>

## <span data-ttu-id="f15aa-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f15aa-129">RELATED LINKS</span></span>

[<span data-ttu-id="f15aa-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f15aa-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="f15aa-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f15aa-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="f15aa-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f15aa-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="f15aa-133">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f15aa-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


