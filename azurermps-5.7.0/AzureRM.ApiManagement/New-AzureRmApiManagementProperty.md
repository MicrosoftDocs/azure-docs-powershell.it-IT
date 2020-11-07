---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688593"
---
# <span data-ttu-id="adf5d-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="adf5d-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="adf5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adf5d-102">SYNOPSIS</span></span>
<span data-ttu-id="adf5d-103">Crea una nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf5d-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adf5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adf5d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adf5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adf5d-105">DESCRIPTION</span></span>
<span data-ttu-id="adf5d-106">Il cmdlet **New-AzureRmApiManagementProperty** crea una **Proprietà** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="adf5d-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="adf5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adf5d-107">EXAMPLES</span></span>

### <span data-ttu-id="adf5d-108">Esempio 1: creare una proprietà che include tag</span><span class="sxs-lookup"><span data-stu-id="adf5d-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="adf5d-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="adf5d-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="adf5d-110">Il secondo comando crea una proprietà e assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf5d-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="adf5d-111">Esempio 2: creare una proprietà con un valore segreto</span><span class="sxs-lookup"><span data-stu-id="adf5d-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="adf5d-112">Questo comando crea una **Proprietà** con un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="adf5d-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="adf5d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adf5d-113">PARAMETERS</span></span>

### <span data-ttu-id="adf5d-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="adf5d-114">-Context</span></span>
<span data-ttu-id="adf5d-115">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="adf5d-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adf5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf5d-116">-DefaultProfile</span></span>
<span data-ttu-id="adf5d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adf5d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="adf5d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="adf5d-118">-Name</span></span>
<span data-ttu-id="adf5d-119">Specifica il nome della proprietà creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adf5d-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="adf5d-120">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="adf5d-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="adf5d-121">I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="adf5d-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="adf5d-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="adf5d-122">-PropertyId</span></span>
<span data-ttu-id="adf5d-123">Specifica un ID per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf5d-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="adf5d-124">La lunghezza massima è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="adf5d-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="adf5d-125">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="adf5d-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="adf5d-126">-Segreto</span><span class="sxs-lookup"><span data-stu-id="adf5d-126">-Secret</span></span>
<span data-ttu-id="adf5d-127">Indica che il valore della proprietà è un segreto e deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="adf5d-127">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adf5d-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="adf5d-128">-Tag</span></span>
<span data-ttu-id="adf5d-129">Tag da associare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf5d-129">Tags to be associated with Property.</span></span> <span data-ttu-id="adf5d-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="adf5d-130">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adf5d-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="adf5d-131">-Value</span></span>
<span data-ttu-id="adf5d-132">Specifica un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf5d-132">Specifies a value for the property.</span></span>
<span data-ttu-id="adf5d-133">Questo valore può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="adf5d-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="adf5d-134">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="adf5d-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="adf5d-135">Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="adf5d-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="adf5d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf5d-136">CommonParameters</span></span>
<span data-ttu-id="adf5d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf5d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf5d-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf5d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf5d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adf5d-139">INPUTS</span></span>

### <span data-ttu-id="adf5d-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="adf5d-140">None</span></span>
<span data-ttu-id="adf5d-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="adf5d-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adf5d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adf5d-142">OUTPUTS</span></span>

### <span data-ttu-id="adf5d-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="adf5d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="adf5d-144">Note</span><span class="sxs-lookup"><span data-stu-id="adf5d-144">NOTES</span></span>

## <span data-ttu-id="adf5d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adf5d-145">RELATED LINKS</span></span>

[<span data-ttu-id="adf5d-146">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="adf5d-146">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="adf5d-147">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="adf5d-147">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


