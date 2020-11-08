---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030852"
---
# <span data-ttu-id="0bdfb-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0bdfb-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="0bdfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bdfb-102">SYNOPSIS</span></span>
<span data-ttu-id="0bdfb-103">Crea un ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="0bdfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bdfb-104">SYNTAX</span></span>

### <span data-ttu-id="0bdfb-105">QuickCreate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bdfb-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0bdfb-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="0bdfb-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0bdfb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bdfb-107">DESCRIPTION</span></span>
<span data-ttu-id="0bdfb-108">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0bdfb-109">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0bdfb-110">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0bdfb-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0bdfb-111">Il cmdlet **New-WAPackVMRole** crea un ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="0bdfb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bdfb-112">EXAMPLES</span></span>

### <span data-ttu-id="0bdfb-113">Esempio 1: creare un ruolo macchina virtuale (emulando il comportamento WAP)</span><span class="sxs-lookup"><span data-stu-id="0bdfb-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="0bdfb-114">Dato che non specifichiamo alcun servizio cloud (emulando il comportamento WAP), il comando creerà un servizio cloud per noi che avrà lo stesso nome del ruolo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="0bdfb-115">In questo caso, il comando seguente creerà un ruolo di macchina virtuale con il nome ContosoVMRole01, label ContosoVMRoleLabel01.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="0bdfb-116">Tieni presente che la definizione della risorsa usata in questo articolo deve essere creata manualmente anche se PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="0bdfb-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bdfb-117">PARAMETERS</span></span>

### <span data-ttu-id="0bdfb-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="0bdfb-118">-CloudService</span></span>
<span data-ttu-id="0bdfb-119">Specifica un servizio cloud per il ruolo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bdfb-120">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="0bdfb-120">-Label</span></span>
<span data-ttu-id="0bdfb-121">Specifica un'etichetta per il ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-121">Specifies a label for the virtual machine role.</span></span>

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

### <span data-ttu-id="0bdfb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0bdfb-122">-Name</span></span>
<span data-ttu-id="0bdfb-123">Specifica un nome per il ruolo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-123">Specifies a name for the virtual machine role.</span></span>

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

### <span data-ttu-id="0bdfb-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="0bdfb-124">-Profile</span></span>
<span data-ttu-id="0bdfb-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0bdfb-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0bdfb-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="0bdfb-127">-ResourceDefinition</span></span>
<span data-ttu-id="0bdfb-128">Specifica una definizione di risorsa per il ruolo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bdfb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bdfb-129">CommonParameters</span></span>
<span data-ttu-id="0bdfb-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bdfb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bdfb-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bdfb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bdfb-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bdfb-132">INPUTS</span></span>

## <span data-ttu-id="0bdfb-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bdfb-133">OUTPUTS</span></span>

## <span data-ttu-id="0bdfb-134">Note</span><span class="sxs-lookup"><span data-stu-id="0bdfb-134">NOTES</span></span>

## <span data-ttu-id="0bdfb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bdfb-135">RELATED LINKS</span></span>

[<span data-ttu-id="0bdfb-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0bdfb-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="0bdfb-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0bdfb-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="0bdfb-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0bdfb-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


