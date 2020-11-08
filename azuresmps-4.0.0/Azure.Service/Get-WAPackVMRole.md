---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030876"
---
# <span data-ttu-id="04437-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="04437-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="04437-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04437-102">SYNOPSIS</span></span>

## <span data-ttu-id="04437-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04437-103">SYNTAX</span></span>

### <span data-ttu-id="04437-104">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04437-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="04437-105">FromName</span><span class="sxs-lookup"><span data-stu-id="04437-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="04437-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="04437-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="04437-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04437-107">DESCRIPTION</span></span>
<span data-ttu-id="04437-108">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="04437-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="04437-109">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="04437-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="04437-110">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="04437-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="04437-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04437-111">EXAMPLES</span></span>

### <span data-ttu-id="04437-112">Esempio 1: ottenere un ruolo macchina virtuale (creato tramite il portale)</span><span class="sxs-lookup"><span data-stu-id="04437-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="04437-113">Questo comando consente di ottenere un ruolo di macchina virtuale creato tramite il portale denominato ContosoVMRole01.</span><span class="sxs-lookup"><span data-stu-id="04437-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="04437-114">Esempio 2: ottenere un ruolo di macchina virtuale usando un nome e un nome del servizio cloud</span><span class="sxs-lookup"><span data-stu-id="04437-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="04437-115">Questo comando ottiene un ruolo di macchina virtuale denominato ContosoVMRole02 che si trova in un servizio cloud denominato ContosoCloudService01.</span><span class="sxs-lookup"><span data-stu-id="04437-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="04437-116">Esempio 3: ottenere tutto il ruolo della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="04437-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="04437-117">Questo comando ottiene tutto il ruolo della macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="04437-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="04437-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04437-118">PARAMETERS</span></span>

### <span data-ttu-id="04437-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="04437-119">-CloudServiceName</span></span>
<span data-ttu-id="04437-120">Specifica il nome del servizio cloud del ruolo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04437-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04437-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="04437-121">-Name</span></span>
<span data-ttu-id="04437-122">Specifica il nome di un ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04437-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04437-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="04437-123">-Profile</span></span>
<span data-ttu-id="04437-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04437-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04437-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="04437-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04437-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04437-126">CommonParameters</span></span>
<span data-ttu-id="04437-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04437-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04437-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04437-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04437-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04437-129">INPUTS</span></span>

## <span data-ttu-id="04437-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04437-130">OUTPUTS</span></span>

## <span data-ttu-id="04437-131">Note</span><span class="sxs-lookup"><span data-stu-id="04437-131">NOTES</span></span>

## <span data-ttu-id="04437-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04437-132">RELATED LINKS</span></span>

[<span data-ttu-id="04437-133">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="04437-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="04437-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="04437-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="04437-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="04437-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


