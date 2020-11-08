---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029697"
---
# <span data-ttu-id="c2414-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c2414-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="c2414-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2414-102">SYNOPSIS</span></span>
<span data-ttu-id="c2414-103">Crea un oggetto di configurazione ACL vuoto.</span><span class="sxs-lookup"><span data-stu-id="c2414-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="c2414-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2414-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c2414-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2414-105">DESCRIPTION</span></span>
<span data-ttu-id="c2414-106">Il cmdlet **New-AzureAclConfig** crea un oggetto di configurazione dell'elenco di controllo di accesso (ACL) vuoto.</span><span class="sxs-lookup"><span data-stu-id="c2414-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="c2414-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2414-107">EXAMPLES</span></span>

### <span data-ttu-id="c2414-108">Esempio 1: creare un oggetto di configurazione ACL</span><span class="sxs-lookup"><span data-stu-id="c2414-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="c2414-109">Questo comando crea un oggetto di configurazione ACL vuoto e lo archivia nella variabile $Acl.</span><span class="sxs-lookup"><span data-stu-id="c2414-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="c2414-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2414-110">PARAMETERS</span></span>

### <span data-ttu-id="c2414-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c2414-111">-InformationAction</span></span>
<span data-ttu-id="c2414-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c2414-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c2414-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2414-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2414-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="c2414-114">Continue</span></span>
- <span data-ttu-id="c2414-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="c2414-115">Ignore</span></span>
- <span data-ttu-id="c2414-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c2414-116">Inquire</span></span>
- <span data-ttu-id="c2414-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c2414-117">SilentlyContinue</span></span>
- <span data-ttu-id="c2414-118">Stop</span><span class="sxs-lookup"><span data-stu-id="c2414-118">Stop</span></span>
- <span data-ttu-id="c2414-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c2414-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2414-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c2414-120">-InformationVariable</span></span>
<span data-ttu-id="c2414-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c2414-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2414-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2414-122">CommonParameters</span></span>
<span data-ttu-id="c2414-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2414-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2414-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2414-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2414-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2414-125">INPUTS</span></span>

## <span data-ttu-id="c2414-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2414-126">OUTPUTS</span></span>

## <span data-ttu-id="c2414-127">Note</span><span class="sxs-lookup"><span data-stu-id="c2414-127">NOTES</span></span>

## <span data-ttu-id="c2414-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2414-128">RELATED LINKS</span></span>

[<span data-ttu-id="c2414-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c2414-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="c2414-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c2414-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="c2414-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c2414-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


