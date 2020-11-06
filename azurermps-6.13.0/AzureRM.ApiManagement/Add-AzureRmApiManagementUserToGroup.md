---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519793"
---
# <span data-ttu-id="acb71-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="acb71-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="acb71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acb71-102">SYNOPSIS</span></span>
<span data-ttu-id="acb71-103">Aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="acb71-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acb71-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acb71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acb71-105">DESCRIPTION</span></span>
<span data-ttu-id="acb71-106">Il cmdlet **Add-AzureRmApiManagementUserToGroup** aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="acb71-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="acb71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acb71-107">EXAMPLES</span></span>

### <span data-ttu-id="acb71-108">Esempio 1: aggiungere un utente a un gruppo</span><span class="sxs-lookup"><span data-stu-id="acb71-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="acb71-109">Questo comando aggiunge un utente esistente a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="acb71-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="acb71-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acb71-110">PARAMETERS</span></span>

### <span data-ttu-id="acb71-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="acb71-111">-Context</span></span>
<span data-ttu-id="acb71-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="acb71-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="acb71-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="acb71-113">This parameter is required.</span></span>

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

### <span data-ttu-id="acb71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb71-114">-DefaultProfile</span></span>
<span data-ttu-id="acb71-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acb71-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acb71-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="acb71-116">-GroupId</span></span>
<span data-ttu-id="acb71-117">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="acb71-117">Specifies the group ID.</span></span>
<span data-ttu-id="acb71-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="acb71-118">This parameter is required.</span></span>

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

### <span data-ttu-id="acb71-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acb71-119">-PassThru</span></span>
<span data-ttu-id="acb71-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="acb71-120">passthru</span></span>

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

### <span data-ttu-id="acb71-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="acb71-121">-UserId</span></span>
<span data-ttu-id="acb71-122">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="acb71-122">Specifies the user ID.</span></span>
<span data-ttu-id="acb71-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="acb71-123">This parameter is required.</span></span>

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

### <span data-ttu-id="acb71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb71-124">CommonParameters</span></span>
<span data-ttu-id="acb71-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acb71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb71-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb71-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb71-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acb71-127">INPUTS</span></span>

### <span data-ttu-id="acb71-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="acb71-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="acb71-129">System. String</span><span class="sxs-lookup"><span data-stu-id="acb71-129">System.String</span></span>

### <span data-ttu-id="acb71-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="acb71-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="acb71-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acb71-131">OUTPUTS</span></span>

### <span data-ttu-id="acb71-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="acb71-132">System.Boolean</span></span>

## <span data-ttu-id="acb71-133">Note</span><span class="sxs-lookup"><span data-stu-id="acb71-133">NOTES</span></span>

## <span data-ttu-id="acb71-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acb71-134">RELATED LINKS</span></span>

[<span data-ttu-id="acb71-135">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="acb71-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="acb71-136">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="acb71-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


