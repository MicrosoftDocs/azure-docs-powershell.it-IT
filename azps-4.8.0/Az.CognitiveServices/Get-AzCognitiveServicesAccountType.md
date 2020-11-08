---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191646"
---
# <span data-ttu-id="6886e-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="6886e-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="6886e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6886e-102">SYNOPSIS</span></span>
<span data-ttu-id="6886e-103">Ottiene i tipi di account dei servizi cognitivi disponibili.</span><span class="sxs-lookup"><span data-stu-id="6886e-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="6886e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6886e-104">SYNTAX</span></span>

### <span data-ttu-id="6886e-105">GetAccountTypes (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6886e-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6886e-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="6886e-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6886e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6886e-107">DESCRIPTION</span></span>
<span data-ttu-id="6886e-108">Il cmdlet **Get-AzCognitiveServicesAccountType** ottiene i tipi di account dei servizi cognitivi disponibili in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6886e-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="6886e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6886e-109">EXAMPLES</span></span>

### <span data-ttu-id="6886e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6886e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="6886e-111">Ottenere l'elenco dei tipi disponibili.</span><span class="sxs-lookup"><span data-stu-id="6886e-111">Get the list of available Types.</span></span>

### <span data-ttu-id="6886e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6886e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="6886e-113">Ottieni l'elenco dei tipi disponibili in westus.</span><span class="sxs-lookup"><span data-stu-id="6886e-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="6886e-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6886e-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="6886e-115">Verificare se `Face` è un nome di tipo valido, il nome verrà restituito se si tratta di un nome valido.</span><span class="sxs-lookup"><span data-stu-id="6886e-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="6886e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6886e-116">PARAMETERS</span></span>

### <span data-ttu-id="6886e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6886e-117">-DefaultProfile</span></span>
<span data-ttu-id="6886e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6886e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6886e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6886e-119">-Location</span></span>
<span data-ttu-id="6886e-120">Posizione dell'account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="6886e-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="6886e-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="6886e-121">-TypeName</span></span>
<span data-ttu-id="6886e-122">Nome del tipo di account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="6886e-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="6886e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6886e-123">CommonParameters</span></span>
<span data-ttu-id="6886e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6886e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6886e-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6886e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6886e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6886e-126">INPUTS</span></span>

### <span data-ttu-id="6886e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6886e-127">System.String</span></span>

## <span data-ttu-id="6886e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6886e-128">OUTPUTS</span></span>

### <span data-ttu-id="6886e-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="6886e-129">System.String[]</span></span>

### <span data-ttu-id="6886e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6886e-130">System.String</span></span>

## <span data-ttu-id="6886e-131">Note</span><span class="sxs-lookup"><span data-stu-id="6886e-131">NOTES</span></span>

## <span data-ttu-id="6886e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6886e-132">RELATED LINKS</span></span>
