---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029970"
---
# <span data-ttu-id="8292c-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="8292c-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="8292c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8292c-102">SYNOPSIS</span></span>
<span data-ttu-id="8292c-103">Ottiene gli oggetti del profilo di dimensione del ruolo Cloud VM.</span><span class="sxs-lookup"><span data-stu-id="8292c-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="8292c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8292c-104">SYNTAX</span></span>

### <span data-ttu-id="8292c-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8292c-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8292c-106">FromName</span><span class="sxs-lookup"><span data-stu-id="8292c-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8292c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8292c-107">DESCRIPTION</span></span>
<span data-ttu-id="8292c-108">Il cmdlet **Get-WAPackCloudVMRoleSizeProfile** ottiene gli oggetti del profilo delle dimensioni del ruolo Cloud VM per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="8292c-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="8292c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8292c-109">EXAMPLES</span></span>

### <span data-ttu-id="8292c-110">Esempio 1: ottenere un profilo di dimensione del ruolo di VM cloud usando un nome</span><span class="sxs-lookup"><span data-stu-id="8292c-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="8292c-111">Questo comando consente di ottenere il profilo delle dimensioni denominato Small.</span><span class="sxs-lookup"><span data-stu-id="8292c-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="8292c-112">Esempio 2: ottenere tutti i profili delle dimensioni del ruolo Cloud VM</span><span class="sxs-lookup"><span data-stu-id="8292c-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="8292c-113">Questo comando ottiene tutti i profili di dimensione.</span><span class="sxs-lookup"><span data-stu-id="8292c-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="8292c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8292c-114">PARAMETERS</span></span>

### <span data-ttu-id="8292c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8292c-115">-Name</span></span>
<span data-ttu-id="8292c-116">Specifica il nome di un profilo di dimensione del ruolo di VM cloud.</span><span class="sxs-lookup"><span data-stu-id="8292c-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8292c-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="8292c-117">-Profile</span></span>
<span data-ttu-id="8292c-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8292c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8292c-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8292c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8292c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8292c-120">CommonParameters</span></span>
<span data-ttu-id="8292c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8292c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8292c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8292c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8292c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8292c-123">INPUTS</span></span>

## <span data-ttu-id="8292c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8292c-124">OUTPUTS</span></span>

## <span data-ttu-id="8292c-125">Note</span><span class="sxs-lookup"><span data-stu-id="8292c-125">NOTES</span></span>

## <span data-ttu-id="8292c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8292c-126">RELATED LINKS</span></span>

[<span data-ttu-id="8292c-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8292c-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


