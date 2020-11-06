---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: bdcbac04d621319ac3837f1efaef52018e0f4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522086"
---
# <span data-ttu-id="36c76-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="36c76-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="36c76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36c76-102">SYNOPSIS</span></span>
<span data-ttu-id="36c76-103">Rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="36c76-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36c76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36c76-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36c76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36c76-105">DESCRIPTION</span></span>
<span data-ttu-id="36c76-106">Il cmdlet **Remove-AzureRmApiManagementUserFromGroup** rimuove un utente da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="36c76-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="36c76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36c76-107">EXAMPLES</span></span>

### <span data-ttu-id="36c76-108">Esempio 1: rimuovere un utente da un gruppo</span><span class="sxs-lookup"><span data-stu-id="36c76-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="36c76-109">Questo comando rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="36c76-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="36c76-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36c76-110">PARAMETERS</span></span>

### <span data-ttu-id="36c76-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="36c76-111">-Context</span></span>
<span data-ttu-id="36c76-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="36c76-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="36c76-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="36c76-113">This parameter is required.</span></span>

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

### <span data-ttu-id="36c76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c76-114">-DefaultProfile</span></span>
<span data-ttu-id="36c76-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36c76-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="36c76-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="36c76-116">-GroupId</span></span>
<span data-ttu-id="36c76-117">Specifica l'ID del gruppo da cui rimuovere un utente.</span><span class="sxs-lookup"><span data-stu-id="36c76-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="36c76-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36c76-118">-PassThru</span></span>
<span data-ttu-id="36c76-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="36c76-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="36c76-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="36c76-120">-UserId</span></span>
<span data-ttu-id="36c76-121">Specifica l'ID dell'utente da rimuovere dal gruppo.</span><span class="sxs-lookup"><span data-stu-id="36c76-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="36c76-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c76-122">CommonParameters</span></span>
<span data-ttu-id="36c76-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c76-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c76-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c76-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c76-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36c76-125">INPUTS</span></span>

### <span data-ttu-id="36c76-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="36c76-126">None</span></span>
<span data-ttu-id="36c76-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="36c76-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36c76-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36c76-128">OUTPUTS</span></span>

### <span data-ttu-id="36c76-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36c76-129">System.Boolean</span></span>

## <span data-ttu-id="36c76-130">Note</span><span class="sxs-lookup"><span data-stu-id="36c76-130">NOTES</span></span>

## <span data-ttu-id="36c76-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36c76-131">RELATED LINKS</span></span>

[<span data-ttu-id="36c76-132">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="36c76-132">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="36c76-133">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="36c76-133">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


