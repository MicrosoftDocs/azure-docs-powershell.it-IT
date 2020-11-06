---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514139"
---
# <span data-ttu-id="68538-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="68538-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="68538-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68538-102">SYNOPSIS</span></span>
<span data-ttu-id="68538-103">Recupera un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68538-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68538-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68538-104">SYNTAX</span></span>

### <span data-ttu-id="68538-105">ApplicationObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68538-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68538-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68538-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68538-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68538-107">DESCRIPTION</span></span>
<span data-ttu-id="68538-108">Il cmdlet Get-AzureRmADAppCredential può essere usato per recuperare un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68538-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="68538-109">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68538-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="68538-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68538-110">EXAMPLES</span></span>

### <span data-ttu-id="68538-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68538-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="68538-112">Restituisce un elenco di credenziali associate all'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="68538-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="68538-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68538-113">PARAMETERS</span></span>

### <span data-ttu-id="68538-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="68538-114">-ApplicationId</span></span>
<span data-ttu-id="68538-115">ID dell'applicazione per cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="68538-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68538-116">-DefaultProfile</span></span>
<span data-ttu-id="68538-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="68538-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68538-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="68538-118">-ObjectId</span></span>
<span data-ttu-id="68538-119">ID oggetto dell'applicazione per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="68538-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68538-120">CommonParameters</span></span>
<span data-ttu-id="68538-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68538-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68538-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68538-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68538-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68538-123">INPUTS</span></span>

### <span data-ttu-id="68538-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="68538-124">None</span></span>
<span data-ttu-id="68538-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="68538-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68538-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68538-126">OUTPUTS</span></span>

### <span data-ttu-id="68538-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="68538-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="68538-128">Note</span><span class="sxs-lookup"><span data-stu-id="68538-128">NOTES</span></span>

## <span data-ttu-id="68538-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68538-129">RELATED LINKS</span></span>

[<span data-ttu-id="68538-130">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="68538-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="68538-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="68538-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="68538-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="68538-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

