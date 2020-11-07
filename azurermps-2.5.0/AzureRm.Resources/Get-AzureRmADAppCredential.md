---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
ms.openlocfilehash: 5390cf033174f473a08a8407028a709a02677352
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866214"
---
# <span data-ttu-id="c080c-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c080c-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="c080c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c080c-102">SYNOPSIS</span></span>
<span data-ttu-id="c080c-103">Recupera un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c080c-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c080c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c080c-104">SYNTAX</span></span>

### <span data-ttu-id="c080c-105">ApplicationObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c080c-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c080c-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c080c-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c080c-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c080c-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c080c-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c080c-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c080c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c080c-109">DESCRIPTION</span></span>
<span data-ttu-id="c080c-110">Il cmdlet Get-AzureRmADAppCredential può essere usato per recuperare un elenco di credenziali associate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c080c-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="c080c-111">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c080c-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="c080c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c080c-112">EXAMPLES</span></span>

### <span data-ttu-id="c080c-113">Esempio 1-ottenere le credenziali dell'applicazione per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="c080c-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="c080c-114">Restituisce un elenco di credenziali associate all'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="c080c-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="c080c-115">Esempio 2-ottenere le credenziali dell'applicazione tramite pipe</span><span class="sxs-lookup"><span data-stu-id="c080c-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="c080c-116">Ottiene l'applicazione con l'ID oggetto "1f99cf81-0146-4f4e-BEAE-2007d0668476" e la convoglia al cmdlet Get-AzureRmADAppCredential per elencare tutte le credenziali per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c080c-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="c080c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c080c-117">PARAMETERS</span></span>

### <span data-ttu-id="c080c-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c080c-118">-ApplicationId</span></span>
<span data-ttu-id="c080c-119">ID dell'applicazione per cui recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="c080c-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="c080c-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c080c-120">-ApplicationObject</span></span>
<span data-ttu-id="c080c-121">L'oggetto Application per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c080c-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="c080c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c080c-122">-DefaultProfile</span></span>
<span data-ttu-id="c080c-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c080c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c080c-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c080c-124">-DisplayName</span></span>
<span data-ttu-id="c080c-125">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c080c-125">The display name of the application.</span></span>

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

### <span data-ttu-id="c080c-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c080c-126">-ObjectId</span></span>
<span data-ttu-id="c080c-127">ID oggetto dell'applicazione per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c080c-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="c080c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c080c-128">CommonParameters</span></span>
<span data-ttu-id="c080c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c080c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c080c-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c080c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c080c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c080c-131">INPUTS</span></span>

### <span data-ttu-id="c080c-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c080c-132">System.Guid</span></span>

### <span data-ttu-id="c080c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c080c-133">System.String</span></span>

### <span data-ttu-id="c080c-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c080c-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="c080c-135">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c080c-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="c080c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c080c-136">OUTPUTS</span></span>

### <span data-ttu-id="c080c-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="c080c-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="c080c-138">Note</span><span class="sxs-lookup"><span data-stu-id="c080c-138">NOTES</span></span>

## <span data-ttu-id="c080c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c080c-139">RELATED LINKS</span></span>

[<span data-ttu-id="c080c-140">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c080c-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="c080c-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c080c-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="c080c-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c080c-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

