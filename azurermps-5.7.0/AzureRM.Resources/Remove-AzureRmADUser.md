---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520401"
---
# <span data-ttu-id="a76c4-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a76c4-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="a76c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a76c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a76c4-103">Elimina un utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a76c4-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a76c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a76c4-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a76c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a76c4-105">DESCRIPTION</span></span>
<span data-ttu-id="a76c4-106">Elimina un utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="a76c4-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="a76c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a76c4-107">EXAMPLES</span></span>

### <span data-ttu-id="a76c4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a76c4-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a76c4-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="a76c4-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="a76c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a76c4-110">PARAMETERS</span></span>

### <span data-ttu-id="a76c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76c4-111">-DefaultProfile</span></span>
<span data-ttu-id="a76c4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a76c4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a76c4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a76c4-113">-Force</span></span>
<span data-ttu-id="a76c4-114">Se specificato, non chiede conferma per l'eliminazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a76c4-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76c4-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="a76c4-115">-UPNOrObjectId</span></span>
<span data-ttu-id="a76c4-116">Nome dell'entità utente o objectId dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a76c4-116">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="a76c4-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a76c4-117">-Confirm</span></span>
<span data-ttu-id="a76c4-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a76c4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76c4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a76c4-119">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a76c4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76c4-120">CommonParameters</span></span>
<span data-ttu-id="a76c4-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a76c4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76c4-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a76c4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76c4-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a76c4-123">INPUTS</span></span>

### <span data-ttu-id="a76c4-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a76c4-124">None</span></span>
<span data-ttu-id="a76c4-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a76c4-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a76c4-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a76c4-126">OUTPUTS</span></span>

## <span data-ttu-id="a76c4-127">Note</span><span class="sxs-lookup"><span data-stu-id="a76c4-127">NOTES</span></span>

## <span data-ttu-id="a76c4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a76c4-128">RELATED LINKS</span></span>

[<span data-ttu-id="a76c4-129">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a76c4-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="a76c4-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a76c4-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="a76c4-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a76c4-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

