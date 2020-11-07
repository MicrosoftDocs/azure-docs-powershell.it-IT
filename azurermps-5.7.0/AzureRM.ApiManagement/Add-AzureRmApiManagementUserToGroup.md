---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687056"
---
# <span data-ttu-id="2a58a-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="2a58a-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="2a58a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a58a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a58a-103">Aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="2a58a-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a58a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a58a-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a58a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a58a-105">DESCRIPTION</span></span>
<span data-ttu-id="2a58a-106">Il cmdlet **Add-AzureRmApiManagementUserToGroup** aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="2a58a-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="2a58a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a58a-107">EXAMPLES</span></span>

### <span data-ttu-id="2a58a-108">Esempio 1: aggiungere un utente a un gruppo</span><span class="sxs-lookup"><span data-stu-id="2a58a-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="2a58a-109">Questo comando aggiunge un utente esistente a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="2a58a-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="2a58a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a58a-110">PARAMETERS</span></span>

### <span data-ttu-id="2a58a-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2a58a-111">-Context</span></span>
<span data-ttu-id="2a58a-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2a58a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2a58a-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a58a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2a58a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a58a-114">-DefaultProfile</span></span>
<span data-ttu-id="2a58a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a58a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2a58a-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2a58a-116">-GroupId</span></span>
<span data-ttu-id="2a58a-117">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="2a58a-117">Specifies the group ID.</span></span>
<span data-ttu-id="2a58a-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a58a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2a58a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a58a-119">-PassThru</span></span>
<span data-ttu-id="2a58a-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="2a58a-120">passthru</span></span>

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

### <span data-ttu-id="2a58a-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="2a58a-121">-UserId</span></span>
<span data-ttu-id="2a58a-122">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="2a58a-122">Specifies the user ID.</span></span>
<span data-ttu-id="2a58a-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a58a-123">This parameter is required.</span></span>

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

### <span data-ttu-id="2a58a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a58a-124">CommonParameters</span></span>
<span data-ttu-id="2a58a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a58a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a58a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a58a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a58a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a58a-127">INPUTS</span></span>

### <span data-ttu-id="2a58a-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2a58a-128">None</span></span>
<span data-ttu-id="2a58a-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2a58a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a58a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a58a-130">OUTPUTS</span></span>

### <span data-ttu-id="2a58a-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="2a58a-131">Boolean</span></span>

## <span data-ttu-id="2a58a-132">Note</span><span class="sxs-lookup"><span data-stu-id="2a58a-132">NOTES</span></span>

## <span data-ttu-id="2a58a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a58a-133">RELATED LINKS</span></span>

[<span data-ttu-id="2a58a-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2a58a-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="2a58a-135">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="2a58a-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


