---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029709"
---
# <span data-ttu-id="0ab27-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="0ab27-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="0ab27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ab27-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab27-103">Disconnette immediatamente una sessione RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab27-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="0ab27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ab27-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ab27-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab27-106">Il cmdlet **Invoke-AzureRemoteAppSessionLogoff** disconnette immediatamente un utente da una sessione remota in uso in Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="0ab27-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="0ab27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ab27-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab27-108">Esempio 1: disconnettersi da un utente</span><span class="sxs-lookup"><span data-stu-id="0ab27-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="0ab27-109">Questo comando disconnette l'utente il cui UPN è PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="0ab27-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="0ab27-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ab27-110">PARAMETERS</span></span>

### <span data-ttu-id="0ab27-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="0ab27-111">-CollectionName</span></span>
<span data-ttu-id="0ab27-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab27-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab27-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="0ab27-113">-Profile</span></span>
<span data-ttu-id="0ab27-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ab27-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ab27-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0ab27-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ab27-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="0ab27-116">-UserUpn</span></span>
<span data-ttu-id="0ab27-117">Specifica il nome dell'entità utente (UPN) di un utente, ad esempio PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="0ab27-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab27-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ab27-118">-Confirm</span></span>
<span data-ttu-id="0ab27-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ab27-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab27-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab27-120">-WhatIf</span></span>
<span data-ttu-id="0ab27-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ab27-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ab27-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ab27-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab27-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab27-123">CommonParameters</span></span>
<span data-ttu-id="0ab27-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab27-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab27-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab27-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab27-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ab27-126">INPUTS</span></span>

## <span data-ttu-id="0ab27-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ab27-127">OUTPUTS</span></span>

## <span data-ttu-id="0ab27-128">Note</span><span class="sxs-lookup"><span data-stu-id="0ab27-128">NOTES</span></span>

## <span data-ttu-id="0ab27-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ab27-129">RELATED LINKS</span></span>

[<span data-ttu-id="0ab27-130">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="0ab27-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="0ab27-131">Disconnetti-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="0ab27-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="0ab27-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="0ab27-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


