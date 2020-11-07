---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687747"
---
# <span data-ttu-id="91966-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91966-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="91966-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91966-102">SYNOPSIS</span></span>
<span data-ttu-id="91966-103">Crea una nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="91966-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91966-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91966-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91966-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91966-105">DESCRIPTION</span></span>
<span data-ttu-id="91966-106">Il cmdlet **New-AzureRmApiManagementProperty** crea una **Proprietà** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="91966-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="91966-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91966-107">EXAMPLES</span></span>

### <span data-ttu-id="91966-108">Esempio 1: creare una proprietà che include tag</span><span class="sxs-lookup"><span data-stu-id="91966-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="91966-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="91966-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="91966-110">Il secondo comando crea una proprietà e assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="91966-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="91966-111">Esempio 2: creare una proprietà con un valore segreto</span><span class="sxs-lookup"><span data-stu-id="91966-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="91966-112">Questo comando crea una **Proprietà** con un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="91966-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="91966-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91966-113">PARAMETERS</span></span>

### <span data-ttu-id="91966-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="91966-114">-Context</span></span>
<span data-ttu-id="91966-115">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="91966-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91966-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="91966-116">-Name</span></span>
<span data-ttu-id="91966-117">Specifica il nome della proprietà creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91966-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="91966-118">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="91966-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="91966-119">I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="91966-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91966-120">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="91966-120">-PropertyId</span></span>
<span data-ttu-id="91966-121">Specifica un ID per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="91966-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="91966-122">La lunghezza massima è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="91966-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="91966-123">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="91966-123">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91966-124">-Segreto</span><span class="sxs-lookup"><span data-stu-id="91966-124">-Secret</span></span>
<span data-ttu-id="91966-125">Indica che il valore della proprietà è un segreto e deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="91966-125">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91966-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="91966-126">-Tags</span></span>
<span data-ttu-id="91966-127">Specifica una matrice di tag che questo cmdlet associa alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="91966-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="91966-128">Puoi usare i tag per filtrare l'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="91966-128">You can use tags to filter the property list.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91966-129">-Valore</span><span class="sxs-lookup"><span data-stu-id="91966-129">-Value</span></span>
<span data-ttu-id="91966-130">Specifica un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="91966-130">Specifies a value for the property.</span></span>
<span data-ttu-id="91966-131">Questo valore può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="91966-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="91966-132">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="91966-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="91966-133">Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="91966-133">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91966-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91966-134">-DefaultProfile</span></span>
<span data-ttu-id="91966-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91966-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91966-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91966-136">CommonParameters</span></span>
<span data-ttu-id="91966-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91966-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91966-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91966-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91966-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91966-139">INPUTS</span></span>

## <span data-ttu-id="91966-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91966-140">OUTPUTS</span></span>

### <span data-ttu-id="91966-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91966-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="91966-142">Note</span><span class="sxs-lookup"><span data-stu-id="91966-142">NOTES</span></span>

## <span data-ttu-id="91966-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91966-143">RELATED LINKS</span></span>

[<span data-ttu-id="91966-144">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91966-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="91966-145">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91966-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


