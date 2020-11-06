---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: ba169c54d2b4664473a0013be52e2d078827dcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514883"
---
# <span data-ttu-id="f2126-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f2126-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="f2126-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2126-102">SYNOPSIS</span></span>
<span data-ttu-id="f2126-103">Recupera un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2126-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2126-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2126-104">SYNTAX</span></span>

### <span data-ttu-id="f2126-105">ApplicationObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2126-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2126-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2126-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2126-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2126-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2126-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2126-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2126-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2126-109">DESCRIPTION</span></span>
<span data-ttu-id="f2126-110">Il cmdlet Get-AzureRmADAppCredential può essere usato per recuperare un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2126-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="f2126-111">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2126-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="f2126-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2126-112">EXAMPLES</span></span>

### <span data-ttu-id="f2126-113">Esempio 1-ottenere le credenziali dell'applicazione per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="f2126-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="f2126-114">Restituisce un elenco di credenziali associate all'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="f2126-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="f2126-115">Esempio 2-ottenere le credenziali dell'applicazione tramite pipe</span><span class="sxs-lookup"><span data-stu-id="f2126-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="f2126-116">Ottiene l'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476" e la convoglia al cmdlet Get-AzureRmADAppCredential per elencare tutte le credenziali per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2126-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="f2126-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2126-117">PARAMETERS</span></span>

### <span data-ttu-id="f2126-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f2126-118">-ApplicationId</span></span>
<span data-ttu-id="f2126-119">ID dell'applicazione per cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="f2126-119">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2126-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="f2126-120">-ApplicationObject</span></span>
<span data-ttu-id="f2126-121">L'oggetto Application per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="f2126-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2126-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2126-122">-DefaultProfile</span></span>
<span data-ttu-id="f2126-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f2126-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2126-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2126-124">-DisplayName</span></span>
<span data-ttu-id="f2126-125">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2126-125">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2126-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f2126-126">-ObjectId</span></span>
<span data-ttu-id="f2126-127">ID oggetto dell'applicazione per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="f2126-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2126-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2126-128">CommonParameters</span></span>
<span data-ttu-id="f2126-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2126-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2126-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2126-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2126-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2126-131">INPUTS</span></span>

### <span data-ttu-id="f2126-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="f2126-132">System.Guid</span></span>

### <span data-ttu-id="f2126-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f2126-133">System.String</span></span>

### <span data-ttu-id="f2126-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f2126-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="f2126-135">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2126-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="f2126-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2126-136">OUTPUTS</span></span>

### <span data-ttu-id="f2126-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="f2126-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="f2126-138">Note</span><span class="sxs-lookup"><span data-stu-id="f2126-138">NOTES</span></span>

## <span data-ttu-id="f2126-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2126-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2126-140">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f2126-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="f2126-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f2126-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="f2126-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f2126-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

