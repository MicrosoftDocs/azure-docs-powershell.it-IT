---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023654"
---
# <span data-ttu-id="5e1c0-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="5e1c0-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="5e1c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1c0-103">Disabilita l'accesso desktop remoto a un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="5e1c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e1c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="5e1c0-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5e1c0-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5e1c0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5e1c0-108">Il comando **Disable-AzureServiceProjectRemoteDesktop Disabilita** l'accesso desktop remoto a un servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="5e1c0-109">Per rendere effettive le modifiche, è necessario pubblicare il servizio usando il cmdlet **Publish-AzureServiceProject** dopo la disattivazione dell'accesso desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="5e1c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-110">EXAMPLES</span></span>

## <span data-ttu-id="5e1c0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-111">PARAMETERS</span></span>

### <span data-ttu-id="5e1c0-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e1c0-112">-PassThru</span></span>
<span data-ttu-id="5e1c0-113">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5e1c0-114">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e1c0-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="5e1c0-115">-Profile</span></span>
<span data-ttu-id="5e1c0-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e1c0-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1c0-118">CommonParameters</span></span>
<span data-ttu-id="5e1c0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1c0-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1c0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1c0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-121">INPUTS</span></span>

## <span data-ttu-id="5e1c0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e1c0-122">OUTPUTS</span></span>

## <span data-ttu-id="5e1c0-123">Note</span><span class="sxs-lookup"><span data-stu-id="5e1c0-123">NOTES</span></span>

## <span data-ttu-id="5e1c0-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-124">RELATED LINKS</span></span>

[<span data-ttu-id="5e1c0-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="5e1c0-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


