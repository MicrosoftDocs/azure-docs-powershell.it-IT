---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519748"
---
# <span data-ttu-id="b3fe5-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="b3fe5-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="b3fe5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fe5-103">Ottiene i tipi di account dei servizi cognitivi disponibili.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3fe5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3fe5-104">SYNTAX</span></span>

### <span data-ttu-id="b3fe5-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="b3fe5-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3fe5-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="b3fe5-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3fe5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3fe5-107">DESCRIPTION</span></span>
<span data-ttu-id="b3fe5-108">Il cmdlet **Get-AzureRmCognitiveServicesAccountType** ottiene i tipi di account dei servizi cognitivi disponibili in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="b3fe5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3fe5-109">EXAMPLES</span></span>

### <span data-ttu-id="b3fe5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3fe5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="b3fe5-111">Ottenere l'elenco dei tipi disponibili.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-111">Get the list of available Types.</span></span>

### <span data-ttu-id="b3fe5-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b3fe5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="b3fe5-113">Ottieni l'elenco dei tipi disponibili in westus.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="b3fe5-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b3fe5-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="b3fe5-115">Verificare se `Face` è un nome di tipo valido, il nome verrà restituito se si tratta di un nome valido.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="b3fe5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3fe5-116">PARAMETERS</span></span>

### <span data-ttu-id="b3fe5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3fe5-117">-DefaultProfile</span></span>
<span data-ttu-id="b3fe5-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3fe5-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b3fe5-119">-Location</span></span>
<span data-ttu-id="b3fe5-120">Posizione dell'account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fe5-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="b3fe5-121">-TypeName</span></span>
<span data-ttu-id="b3fe5-122">Nome del tipo di account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fe5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fe5-123">CommonParameters</span></span>
<span data-ttu-id="b3fe5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3fe5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3fe5-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3fe5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fe5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3fe5-126">INPUTS</span></span>

### <span data-ttu-id="b3fe5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b3fe5-127">System.String</span></span>

## <span data-ttu-id="b3fe5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3fe5-128">OUTPUTS</span></span>

### <span data-ttu-id="b3fe5-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="b3fe5-129">System.String[]</span></span>

### <span data-ttu-id="b3fe5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b3fe5-130">System.String</span></span>

## <span data-ttu-id="b3fe5-131">Note</span><span class="sxs-lookup"><span data-stu-id="b3fe5-131">NOTES</span></span>

## <span data-ttu-id="b3fe5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3fe5-132">RELATED LINKS</span></span>
